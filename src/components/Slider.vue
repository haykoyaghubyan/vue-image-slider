<template>
<div>
    <transition-group name='fade' tag='div'>
        <div v-for="i in [currentIndex]" :key='i'>
            <img :src="currentImg" />
        </div>
    </transition-group>
    <a class="prev" @click="prev" href='#'>&#10094;</a>
    <a class="next" @click="next" href='#'>&#10095;</a>
</div>
</template>

<script>
export default {
 name: 'Slider',
 data() {
  return {
   timer: null,
   currentIndex: 0,
  }
 },
 props: {
  images: Array,
  intervalVal: Number
 },

 mounted: function() {
  this.startSlide();
 },

 methods: {
  startSlide: function() {
   this.timer = setInterval(this.next, this.intervalVal);
  },


  next: function() {
   this.currentIndex += 1
  },
  prev: function() {
   this.currentIndex -= 1
  }
 },

 computed: {
  currentImg: function() {
   return this.images[Math.abs(this.currentIndex) % this.images.length];
  }
 }

}
</script>

<style>
.fade-enter-active, .fade-leave-active {
     transition: all 0.9s ease;
     overflow: hidden;
     visibility: visible;
     position: absolute;
     width:100%;
     opacity: 1;
}
 .fade-enter, .fade-leave-to {
     visibility: hidden;
     width:100%;
     opacity: 0;
}
 img {
     height:600px;
     width:100% 
}
 .prev, .next {
     cursor: pointer;
     position: absolute;
     top: 40%;
     width: auto;
     padding: 16px;
     color: white;
     font-weight: bold;
     font-size: 18px;
     transition: 0.7s ease;
     border-radius: 0 4px 4px 0;
     text-decoration: none;
     user-select: none;
}
 .next {
     right: 0;
}
 .prev {
     left: 0;
}
 .prev:hover, .next:hover {
     background-color: rgba(0,0,0,0.9);
}

</style>
