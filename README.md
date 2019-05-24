# zhihu_unfollow

复制 zhihu_unfollow.js 中的代码，如下：
'''javascript
i = 1;
function unfollow() {
  window.scrollTo(0, document.body.scrollHeight);
  setTimeout(function() {
    let follow_link = document.querySelectorAll('.follow-link.zg-unfollow.meta-item');
    follow_link[0].click();
    unfollow()
    console.log('取消关注' + i +'个问题');
    i++;
  }, 500)
}
unfollow()
'''
在 https://www.zhihu.com/question/following 执行脚本。

会自动取消所有关注的问题。
