<template>
	<AppContent>
		<div class="welcome-content">
			<h2>{{ t('notes', 'Notes') }}</h2>
			<div class="feature icon-add">
				{{ t('notes', 'Start writing a note by clicking on “{newnote}” in the app navigation.', { newnote: t('notes', 'New note') }) }}
			</div>
			<div class="feature icon-fullscreen">
				{{ t('notes', 'Write down your thoughts without any distractions.') }}
			</div>
			<div class="feature icon-toggle-filelist">
				{{ t('notes', 'Use Markdown markups to style your text.') }}
			</div>
			<div class="feature icon-files-dark">
				{{ t('notes', 'Organize your notes in categories.') }}
			</div>
			<div class="feature icon-phone">
				{{ t('notes', 'Install the app for your mobile phone in order to access your notes from everywhere.') }}
				<br>
				<a href="https://f-droid.org/repository/browse/?fdid=it.niedermann.owncloud.notes" target="_blank"><img :src="imagePath('badges/fdroid.png')" height="80" alt="Get it on F-Droid"></a>
				<a href="https://play.google.com/store/apps/details?id=it.niedermann.owncloud.notes" target="_blank"><img :src="imagePath('badges/play.png')" height="80" alt="Get it on Play Store"></a>
				<a href="https://apps.apple.com/app/cloudnotes-owncloud-notes/id813973264" target="_blank"><img :src="imagePath('badges/app-store.png')" height="80" alt="Download on the App Store"></a>
			</div>
		</div>
	</AppContent>
</template>
<script>

import {
	AppContent,
} from '@nextcloud/vue'

export default {
	name: 'Welcome',

	components: {
		AppContent,
	},

	methods: {
		imagePath(img) {
			return OC.imagePath('notes', img)
		},
	},
}

</script>
<style>
.welcome-content {
	padding: 2em 3em;
}

.welcome-content h2 {
	margin-bottom: 1em;
}

.feature {
	background-position: left top;
	min-height: 32px;
	padding-left: 32px;
	margin-top: 1em;
}

.feature ul {
	list-style: circle outside;
	padding-left: 2em;
}
</style>
