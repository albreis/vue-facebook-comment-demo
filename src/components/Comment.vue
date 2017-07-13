<template>
  <div>
    <div class="fb-comments" data-href="https://developers.facebook.com/docs/plugins/comments#configurator" data-width="100%" data-numposts="5"></div>
  </div>
</template>

<script>

  export default {
    name: "comment",
    created() {

      // Kiểm tra hàm đã tồn tại hay chưa, chưa có thì mới tạo, ko sẽ chạy render 2 lần.
      if (!window.fbAsyncInit) {

        window.fbAsyncInit = function() {
          if (typeof(FB) != 'undefined' && FB != null ) {
            FB.init({
              appId            : 'xxxxxxxxxxxxxxxxxx',
              autoLogAppEvents : true,
              xfbml            : true,
              version          : 'v2.9'
            });
            FB.AppEvents.logPageView();
          }
        };

      }
      else
        window.fbAsyncInit();

    }
  }
</script>
