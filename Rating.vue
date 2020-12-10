<template>
    <div class="rating">
        <div class="stars">
            <template v-for= "n in 5">
                <svg v-if="isHalf(n)" :key="n" viewBox="0 0 24 24" class="star">
                    <path d="M12,15.4V6.1L13.71,10.13L18.09,10.5L14.77,13.39L15.76,17.67M22,9.24L14.81,8.63L12,2L9.19,
8.63L2,9.24L7.45,13.97L5.82,21L12,17.27L18.18,21L16.54,13.97L22,9.24Z" />
                </svg>

                 <svg v-else-if="isFull(n)" :key="n" viewBox="0 0 24 24" class="star">  
                      <path d="M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z"/>
                 </svg> 

                 <svg v-else :key="n" viewBox="002424" class="star">
                     <pathd="M12,15.39L8.24,17.66L9.23,13.38L5.91,10.5L10.29,10.13L12,6.09L13.71,10.13L18.09,10.5L14.77,13.38L15.76,17.66M22,9.24L14.81,8.63L12,2L9.19,8.63L2,9.24L7.45,13.97L5.82,21L12,17.27L18.18,21L16.54,13.97L22,9.24Z"/>
                 </svg>
            </template>
        </div>
        <span v-if="count||count===0" class="count">
            ({{count.toFixed(0)}})
        </span>
    </div>
</template>

<script>
export default {
    name:'Rating',
    props:{
        value:{
            type:Number,
            required:true,
            },

         count:{
             type:Number,
             default:null,
             },
            },

        methods:{
            isHalf(number){
                return this.value > number -1 && this.value < number
                },

                isFull(number){
                    return number <= this.value
            },
      },
  }
</script>

<style scoped>
.rating{
    display:inline-grid;
    grid-auto-flow:column;
    place-items:center;
    gap:0.5rem;
}

.rating.stars{
    display:inline-grid;
    grid-auto-flow:column;
    place-items:center;
    color:#e0b908;
}

.rating .stars .star{
    width:20px;
    height:20px;
    fill:currentColor;
}

.rating.count{
    font-size:0.875rem;
    color:#0008;
}
</style>