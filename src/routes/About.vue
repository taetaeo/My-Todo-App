<template>
  <div class="about">
    <div class="photo">
      <img 
        :src="image" 
        alt="name">
    </div>
    <div class="name">
      {{ name }}
    </div>
    <div class="email">
      {{ email }}
    </div>
    <div class="blog">
      {{ blog }}
    </div>
    <div class="phone">
      {{ phone }}
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    image(){
      return this.$store.state.about.image
    },
    name(){
      return this.$store.state.about.name
    },
    email(){
      return this.$store.state.about.email
    },
    blog(){
      return this.$store.state.about.blog
    },
    phone(){
      return this.$store.state.about.phone
    }
  },
}
</script>
<style lang="scss" scoped>
@import "~/scss/main.scss";

.about{
  text-align:center; // 글자를 가운데 정렬
  .photo{
    width:250px;
    height:250px;
    margin:40px auto 20px;
    padding:30px;
    border:10px solid $gray-300;
    border-radius:50%;
    box-sizing: border-box;
    background-color: $gray-200;
    position:relative;
    img{
      width:100%;
      border-radius: 50%;
      height:100%;
    }
  }
  .name{
    font-size:40px;
    font-family: "Oswald", sans-serif ;
    margin-bottom : 20px;

  }
  .email{
    font-size:16px;
  }
  .blog{
    font-size:16px;
  }
  .phone{
    font-size:16px;
  }
}

</style>