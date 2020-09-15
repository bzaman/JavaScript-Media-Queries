# JavaScript-Media-Queries
Determine if the document matches the media query string in JavaScript.

```Js 
// create function
function mediaQuery(minMaxWidth = 'min', measure = 768, callBack) {
  var mq = window.matchMedia(`(${minMaxWidth}-width: ${measure}px)`);
  function mediaQueryChange(e) {
    if (e.matches) {
      callBack();
    }
  };
  mq.addListener(mediaQueryChange)
  mediaQueryChange(mq)
};

// Call and do your stuff...

 mediaQuery('max', 767, function(){
   console.log('max test...');
 });

 mediaQuery('min', 900, function(){
   console.log('min test...');
 });

```
