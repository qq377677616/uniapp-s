<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import url("./static/css/base.css");
	@import url("./static/css/iconfont.css");
	uni-page-body{min-height:100%;background: #f8f8f8;}
	/* .uni-body{background: #f8f8f8;} */
  .uni-page-head{box-shadow: 0 0 8px 0 #999;}
</style>
