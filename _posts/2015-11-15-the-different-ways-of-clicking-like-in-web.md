---
layout: post
title: "Web 中的各种点赞方式"
description: ""
category: web
tags: [web]
---
{% include JB/setup %}

一些点赞方式整理。
<!-- more -->

- Google+
	
	![Google plus](/assets/images/web/click-like/GooglePlus-like.png)
	![Google plus clicked](/assets/images/web/click-like/GooglePlus-like-clicked.png)

	Google+ 使用的是 `<div>` 标签，当鼠标 hover 时显示 tip。点 + 之后，更改数字和颜色。
	
		<!-- 
			aria-pressed: 标记是否被点赞
			data-tooltip：tip 显示的文本
		-->
		<div id="xxxx" href="javascript:void(0);" tabindex="0" role="button" jscontroller="qG1h8c" jsaction="click:xxx:xxx;" class="esw qk Gc eswd" 
			g:token="xxxx" g:entity="buzz:xxxxx"
			aria-pressed="false" aria-label="为此信息 +1" 
			data-tooltip="为此信息 +1">
			<span dir="ltr" class="tf yda">
				<!-- 
					gr: 加号
					H3：点赞数量
				-->
				<span class="gr"></span>
				<span class="H3" jsname="NnAfwf">356</span>
			</span>
		</div>

- Facebook
	
	![Facebook like](/assets/images/web/click-like/Facebook-like.png)
	
	![Facebook like clicked](/assets/images/web/click-like/Facebook-like-clicked.png)
	
	Facebook 在点击喜欢时，主要是更新样式和文字。

		<span>
			<a data-reactroot="" class="UFILikeLink" href="#" role="button" aria-label="Like this" aria-live="polite" data-ft="{&quot;tn&quot;:&quot;>&quot;}">
				<i class="UFILikeLinkIcon img sp_Ac4x6FflI2r sx_a44ffe"></i>
				<span>Like</span>
			</a>
		</span>

- Pinterest

	![Pinterest like](/assets/images/web/click-like/Pinterest-like.png)
	
	![Pinterest like clicked](/assets/images/web/click-like/Pinterest-like-clicked.png)
	Pinterest 使用了两个 `<button>` 标签，一个用来嵌入心形 icon，一个用来标记喜欢的数量。当点击喜欢的时候，会短暂出现 loading icon 替换心形icon，并设置 button 为 disable，防止连续点击，loading 过后数量加一。
		
		<button class="Button LikeButton Module PinLikeButton btn hasText like leftRounded pinActionBarButton  medium rounded" data-element-type="1" data-source-interest-id="" type="button">
			<!--em 嵌入icon -->
			<em></em>
			<span class="buttonText">Like</span>			 
		</button>
		<button class="Button IncrementingNavigateButton Module NavigateButton btn hasText medium repinLikeNavigateButton like leftRounded pinActionBarButton  rounded" data-element-type="175" type="button">
			<!--span 标记数量 -->
			<span class="buttonText">1</span>  
		</button>
	
- Twitter

	![Twitter like](/assets/images/web/click-like/Twitter-like.png)
	
	![Twitter like clicked](/assets/images/web/click-like/Twitter-like-clicked.png)

	Twitter 在点击喜欢时候，会弹出动画效果；然后更新样式和数据

		<button class="ProfileTweet-actionButton js-actionButton js-actionFavorite" type="button">
			<div class="IconContainer js-tooltip" data-original-title="Like">
				<div class="HeartAnimationContainer">
					<div class="HeartAnimation"></div>
				</div>
				<span class="u-hiddenVisually">Like</span>
			</div>
				<div class="IconTextContainer">
					<span class="ProfileTweet-actionCount" data-tweet-stat-count="143">
						<span class="ProfileTweet-actionCountForPresentation" aria-hidden="true">143</span>
					</span>
				</div>
		</button>
		
- QQZone

	![QQZone like](/assets/images/web/click-like/QQZone-like.png)
	
	![QQZone like clicked](/assets/images/web/click-like/QQZone-like-clicked.png)
	
		<a class="item qz_like_btn_v3" data-islike="0" data-likecnt="0" data-showcount="0" data-unikey="#" data-curkey="#" data-clicklog="like" href="javascript:;">
			<i class="ui-icon icon-praise"></i>赞
		</a>
		
- Douban

	![Douban like](/assets/images/web/click-like/Douban-like.png)
	
	![Douban like clicked](/assets/images/web/click-like/Douban-like-clicked.png)
	
	Douban 点击喜欢的时候，会弹出一个 form 用于添加标签。

		<div class="sns-bar-fav ">
			<span class="fav-num" data-tid="" data-tkind="">
				<a href="#">1330人</a>喜欢
			</span>
			<a class="btn-fav fav-add" title="标为喜欢?" href="#">喜欢</a>
			<script type="text/template" id="fav-tag-template">
				<form action="" method="POST">
					<div style="display:none;"><input type="hidden" name="ck" value="pqpc"/></div>
				</form>
			</script>
		</div>

