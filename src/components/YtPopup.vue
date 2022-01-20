<template>
  <div className="YtPopup center-item" @click="() => {closePopup()}">
            <iframe
                :src="embedLink"
                title="YouTube video player"
                frameBorder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowFullScreen
            ></iframe>
        </div>
</template>

<script>
export default {
	props: {
		closePopup: Function,
		embedLink: String
	}
}
</script>