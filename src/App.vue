<template lang="pug">
  #app
    b-navbar(toggleable='lg' type='dark' variant='info')
      b-container
        b-navbar-brand(to='/') 番茄鐘
        b-navbar-toggle(target='nav-collapse')
        b-collapse#nav-collapse(is-nav)
          b-navbar-nav
            //- https://bootstrap-vue.org/docs/components/nav#comp-ref-b-nav-item
            //- active-class 啟用頁面時要套用 active-class，文字顏色變化，讓使用者知道目前在哪一頁
            b-nav-item(to='/list' active-class="active") 待辦
            b-nav-item(to='/settings' active-class="active") 設定
    //- 避免元件在換頁時被銷毀
    keep-alive
      router-view
</template>
