<template>
	<div class="publiclist2">
		<ul>
			<li v-for="(item,index) in list" :key='index' @click="tiaofn(item.tiaourl)">
				<img :src="item.url" />
				<div class="content">
					<div class="top">
						<h1 v-text="item.title"></h1>
						<p class="cont" v-text="item.cont"></p>
					</div>
					<div class="timer">
						<p v-for="(it,ind) in item.timer" :key='ind' v-text="it"></p>
					</div>
				</div>
				<p class="timer" v-text="item.cishu+'万'"></p>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: "publiclist2",
		props: {
			list: {
				default () {
					return [{
						url: '/static/自己切图/娱乐/entertainment1.png',
						title: '大牌驾到',
						cont: '谁能请动半个娱乐圈，谁能请动娱乐圈明星大碗范冰冰 黄晓明 谢霆锋 .......',
						timer: ['00:42',0],
						cishu: '2683',
						tiaourl:''
					}]
				}
			}
		},
		methods:{
			tiaofn(val){
				alert('tiaozhuan'+val)
			}
		}
	}
</script>

<style scoped>
	.publiclist2>ul{
		padding-left: .17rem;
	}
	.publiclist2>ul>li {
		padding: .2rem .15rem .15rem 0;
		display: flex;
		align-items: stretch;
		border-bottom: .01rem solid #ccc;
	}

	.publiclist2>ul>li>img {
		width: 2.1rem;
		margin-right: .18rem;
	}
	.publiclist2>ul>li>.content{
		width: 2.97rem;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	.publiclist2>ul>li>.content>.top>h1{
		font-size: .24rem;     
		line-height: .3rem;    
		margin-top: .12rem;    
	}                          
	.publiclist2>ul>li>.content>.top>.cont{
		font-size: .14rem;
		line-height: .28rem;
		margin-top: .06rem;
		color: #999;
	}
	.publiclist2>ul>li>.content>.timer{
		display: flex;
		height: .3rem;
		margin-bottom: .06rem;
		align-items: center;
	}
	.publiclist2>ul>li>.content>.timer>p{
		height: .2rem;
		padding-left: .25rem;
		margin-right: .2rem;
		color: #999;
	}
	.publiclist2>ul>li>.timer{
		color: #999;
		font-size: .14rem;
		line-height: .16rem;
		padding-right: .2rem;
		align-self: flex-end;
		background:url(../../../static/自己切图/娱乐/yule_icon1.png) no-repeat center right;
		background-size: .14rem .16rem;
	}
	.publiclist2>ul>li>.timer>p{
		/* background */
	}
</style>
