<template>
	<div id="app" :class="{blackbg: blackBg}">
		<v-header></v-header>
		<div class="container">
			<router-view></router-view>
		</div>
		<v-footer></v-footer>
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
	computed: {
		blackBg() {
			return true;
		}
	}
}
</script>

<style lang="scss">
@font-face {
	font-family: 'icon';
	/* project id 285311 */
	src: url('//at.alicdn.com/t/font_uxc8gojl4rifi529.eot');
	src: url('//at.alicdn.com/t/font_uxc8gojl4rifi529.eot?#iefix') format('embedded-opentype'),
	url('//at.alicdn.com/t/font_uxc8gojl4rifi529.woff') format('woff'),
	url('//at.alicdn.com/t/font_uxc8gojl4rifi529.ttf') format('truetype'),
	url('//at.alicdn.com/t/font_uxc8gojl4rifi529.svg#iconfont') format('svg');
}

#app {
	font-family: 'Avenir', 'PingFang SC', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	display: flex;
	flex-direction: column;
	height: 100%;
	.container {
		flex: 1;
		overflow: auto;
		overflow-x: hidden;
	}
	&.blackbg {
		background-color: rgb(41, 42, 43);
		color: #fff;
	}
}
</style>
