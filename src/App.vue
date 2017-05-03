<template>
	<div id="app" :class="{blackbg: blackBg}">
		<v-header></v-header>
		<div class="container">
			<router-view></router-view>
		</div>
		<v-footer></v-footer>
		<div class="bg_player_mask"></div>
		<div class="bg_player" :style="{ backgroundImage: 'url(' + backgroundImage + ')' }"></div>
	</div>
</template>

<script>
import VHeader from '@/components/header.vue'
import VFooter from '@/components/footer.vue'
export default {
	name: 'app',
	components: {
		VHeader,
		VFooter
	},
	data() {
		return {
			backgroundImage: 'https://avatars2.githubusercontent.com/u/16360684?v=3&s=460'
		}
	},
	computed: {
		blackBg() {
			return false;
		}
	}
}
</script>

<style lang="scss">
@font-face {
  font-family: 'iconfont';  /* project id 285311 */
  src: url('//at.alicdn.com/t/font_ir3es9nr8q4r6bt9.eot');
  src: url('//at.alicdn.com/t/font_ir3es9nr8q4r6bt9.eot?#iefix') format('embedded-opentype'),
  url('//at.alicdn.com/t/font_ir3es9nr8q4r6bt9.woff') format('woff'),
  url('//at.alicdn.com/t/font_ir3es9nr8q4r6bt9.ttf') format('truetype'),
  url('//at.alicdn.com/t/font_ir3es9nr8q4r6bt9.svg#iconfont') format('svg');
}

.icon {
	font-family: "iconfont" !important;
  	font-size: 18px;
  	font-style: normal;
	color: #bdbdbe;
    color: rgba(225,225,225,.8);
}

#app {
	font-family: 'Avenir', 'PingFang SC', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	font-size: 14px;
	display: flex;
	flex-direction: column;
	height: 100%;
	.container {
		flex: 1;
		overflow: auto;
		overflow-x: hidden;
		margin-bottom: 20px;
	}
	&.blackbg {
		background-color: rgb(41, 42, 43);
		color: #fff;
	}
	.bg_player_mask,.bg_player {
		position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
	}
	.bg_player_mask {
		background-color: rgba(0,0,0,.35);
        z-index: -1;
	}
	.bg_player {
		background-repeat: no-repeat;
		background-size: contain;
		background-position: 50%;
		filter: blur(65px);
		opacity: .6;
        z-index: -2;
	}
}
</style>
