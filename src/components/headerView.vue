<template>
  <header id="header">
      <h1><img :src="`./img/logo.svg`" alt="" /></h1>
      <nav class="navbar">
        <div class="navTop">
          <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
          <a href="#"><i class="fa-regular fa-user"></i></a>
          <a href="#"><i class="fa-brands fa-facebook"></i></a>
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
          <a href="#"><i class="fa-brands fa-youtube"></i></a>
          <a href="#"><i class="fa-solid fa-bars"></i></a>
        </div>
        <div class="navMenu">
            <ul>
                <li><a href="#">제이제이코리아</a></li>
                <li><a href="#">투명경영</a></li>
                <li><a href="#">교육사업</a></li>
                <li><a href="#">기관소식</a></li>
                <li><a href="#">후원하기</a></li>
            </ul>
        </div>
      </nav>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss">
#header {
    width: 1200px; margin: 0 auto; 
    display: flex;

    h1 {
      width: 200px; height: 100%;
      img {
        width: 100%;
        padding: 10px 0;
      }
    }
    .navbar{
        display: flex; flex-direction: column;
        margin-left: auto; gap: 5px;
        .navTop{
            font-size: 1.2em;
            margin-left: auto;
            a{padding: 0 5px;}
        }
        .navMenu{
           ul{
            display: flex;
            li{
                a{
                    font-size: 1.3em;
                    display: flex; padding: 0 10px;
                    font-weight: bold;

                }
            }
           }
        }
    }
}
</style>