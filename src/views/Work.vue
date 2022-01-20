<template>
  <div className="Work">
            <YtPopup v-if="ytActive" :embedLink="embedLink" :closePopup="closePopup" />
            <section className="Work__title center-item">
                <div>
                    <h1>Work</h1>
                    <p>Unser ganzer Solz: Unsere Produktionen.</p>
                    <p>Sehen sie sich ein Beispiel unserer Arbeit an!</p>
                </div>
            </section>
            <section className="Work__content__container">
                <div className="Work__navigation">
                    <div
                        id="Work__indicator"
                        ref="workIndicator"
                    ></div>
                    <ul role="list">
                        <li
                            className="Work--active"
                            @click='handleThemeChange($event, "show all")'
                            data-index="0"
                        >
                            SHOW ALL
                        </li>
                        <li
                            @click='handleThemeChange($event, "image")'
                            data-index="1"
                        >
                            IMAGE
                        </li>
                        <li
                            @click='handleThemeChange($event, "action")'
                            data-index="2"
                        >
                            ACTION
                        </li>
                        <li
                            @click='handleThemeChange($event, "outdoor")'
                            data-index="3"
                        >
                            OUTDOOR
                        </li>
                        <li
                            @click='handleThemeChange($event, "animation")'
                            data-index="4"
                        >
                            ANIMATION
                        </li>
                    </ul>
                </div>
                <div className="Work__content wrapper" ref="contentWrapper">
                            <Project 
							v-for="value in projectList.slice(0, 21)"
                                :key="value.title"
                                :projectImage="value.image"
                                :projectTitle="value.title"
                                :projectVideoLink="value.video"
                                :projectTheme="value.theme"
                                :setEmbed="setEmbed"
                            />
                </div>
            </section>
        </div>
</template>

<script>
import projectList from "@/assets/json/ProjectList.json";
import Project from "@/components/Project.vue"
import YtPopup from "@/components/YtPopup.vue"
export default {
	components: {
		Project,
		YtPopup
	},
	data() {
		return {
			projectList,
			ytActive: false,
			embedLink: "",
			rows: 2
		}
	},
	mounted() {
		this.setWorkIndicator();
		this.displayTheme("show all");
		window.onresize = this.handleResize;

	},
	unmounted() {
		window.onresize = null;
	},
	methods: {
		setEmbed(embed) {
			this.embedLink = embed;
			this.ytActive = true;
		},
		closePopup() {
			this.ytActive = false;
			this.embedLink = "";
		},
		displayTheme(theme) {
			let activeProjects =
				theme === "show all"
					? document.querySelectorAll(".Project")
					: document.querySelectorAll(`.Project[data-theme=${theme}]`);
			let inactiveProjects =
				theme === "show all"
					? null
					: document.querySelectorAll(
						`.Project:not([data-theme=${theme}])`
					);

			if (!activeProjects && !inactiveProjects) return;
			if (inactiveProjects) {
				for (const project of inactiveProjects) {
					project.dataset.active = false;
					project.style.opacity = 0;
					project.style.pointerEvents = "none";
				}
			}

			if (activeProjects) {
				let aciveCollumIndex = 0;
				let activeRowIndex = 0;
				for (const project of activeProjects) {
					project.dataset.active = true;
					project.style.opacity = 1;
					project.style.pointerEvents = "initial";
					project.style.left = aciveCollumIndex * 33.33 + "%";
					project.style.top =
						activeProjects?.[0]?.offsetWidth * activeRowIndex + "px";
					aciveCollumIndex++;
					if (aciveCollumIndex >= 3) {
						aciveCollumIndex = 0;
						activeRowIndex++;
					}
				}
			}

			this.rows = Math.ceil(activeProjects.length / 3);
			this.$refs.contentWrapper.style.height = `${
				(this.rows * this.$refs.contentWrapper.offsetWidth) / 3
			}px`;
		},
		setWorkIndicator() {
			let item = document.querySelector(".Work--active");
			this.$refs.workIndicator.style.transform = `translateX(${item.offsetLeft}px)`;
			this.$refs.workIndicator.style.width = `${item.offsetWidth}px`;
		},
		handleThemeChange(e, theme) {
			this.displayTheme(theme);
			document.getElementsByClassName("Work--active")[0].classList.remove("Work--active");
			e.target.classList.add("Work--active");
			this.setWorkIndicator();
		},
		handleResize() {
			let projects = document.querySelectorAll(".Project[data-active=true]");
			if (!projects) return;
			let aciveCollumIndex = 0;
			let activeRowIndex = 0;
			let width = projects[0].offsetWidth; 
			for (const project of projects) {
				project.style.top = activeRowIndex * width + "px";
				aciveCollumIndex++;
				if (aciveCollumIndex >= 3) {
					aciveCollumIndex = 0;
					activeRowIndex++;
				}
			}
			this.$refs.contentWrapper.style.height = `${
				(this.rows * width)
			}px`;
		}
	}

}
</script>
