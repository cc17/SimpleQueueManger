#简单的队列控制器

## 目的：将某些异步操作变得看起来像同步操作，是流程一目了然

### 提供两个简答的demo

* demo1
  ~~~js
   
   var q = new QueueManger();
	q.queue(function(){
		console.log(1);
	}).wait(3000).queue(function(){
		console.log(2);
	}).queue(function(){
		console.log(3);
	}).dequeue().queue(function(){
		console.log('last');
	});
   




* demo2

~~~js
   
   var box = document.getElementById('box');
   var q2 = new QueueManger();
	q2.queue(function(){
		box.setAttribute('class','ani1');
	}).wait(1000).queue(function(){
		box.setAttribute('class','ani2');
	}).dequeue();
   

