<template>
  <div className="Profile wrapper">
            <div className="Profile__content__wrapper">
                <h2 className="Profile__name">{{name}}</h2>
                <p className="Profile__position">{{position}}</p>
                <p className="Profile__description">{{description}}</p>
                <p className="Profile__second__description">
                    {{secondDescription}}
                </p>
                <hr />
                <div className="Profile__social__wrapper">
                    <div className="Profile__btns">
                        <button className="Profile__git__btn">
                            GET IN TOUCH
                        </button>
                        <button className="btn--filled">HIRE ME</button>
                    </div>
                    <div className="Profile__social__links">
                        <span>FOLLOW ME</span>
                        <div className="Profile__social__icon__wrapper center-item">
                            <i className="fab fa-facebook"></i>
                        </div>
                        <div className="Profile__social__icon__wrapper center-item">
                            <i className="fab fa-twitter"></i>
                        </div>
                        <div className="Profile__social__icon__wrapper center-item">
                            <i className="fab fa-linkedin"></i>
                        </div>
                    </div>
                </div>
            </div>
            <div className="Profile__image__wrapper">
                <img :src="require(`@/assets/${image}`)" :alt="name" />
            </div>
        </div>
</template>

<script>
export default {
	props: {
		name: String,
		position: String,
		description: String,
		secondDescription: String,
		image: String,
	},
	mounted() {
		let imageCallback = (entries) => {
            entries.forEach((entry) => {
                if (!entry.isIntersecting) return;
                entry.target.style.animationPlayState = "running";
            });
        };

        let textCallback = (entries) => {
            entries.forEach((entry) => {
                if (!entry.isIntersecting) return;
                entry.target.style.animationPlayState = "running";
            });
        };

        let imageOptions = {
            threshold: 0.2,
        };

        let textOptions = {
            threshold: 0.3,
        };

        let imageObserver = new IntersectionObserver(
            imageCallback,
            imageOptions
        );

        let textObserver = new IntersectionObserver(textCallback, textOptions);

        let profiles = document.getElementsByClassName("Profile");

        let loopIndex = 0;
        for (let profile of profiles) {
            for (let text of profile.children[0].children) {
                // console.log((text.style.animationPlayState = "running"));
                text.style.setProperty(
                    "--silde-delay",
                    loopIndex * 0.1 + 0.4 + "s"
                );
                loopIndex++;
                textObserver.observe(text);
            }
            loopIndex = 0;
            imageObserver.observe(profile.children[1]);
        }
	},
}
</script>

<style>

</style>