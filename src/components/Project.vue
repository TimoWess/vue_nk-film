<template>
   <div
        className="Project"
        :data-theme="projectTheme"
    >
        <img :src="require('@/assets/'+projectImage)" alt="" />
        <div className="Project__title__info">
            <p>{{projectTitle}}</p>
            <button v-if="projectVideoLink" className="btn--filled">WATCH</button>
        </div>
    </div>
</template>

<script>
export default {
	props: {
		setEmbde: Function,
		projectVideoLink: String,
		projectTitle: String,
		projectImage: String,
		projectTheme: String,
	}
}
</script>