<template>
  <div>
  	{{ a }}
  </div>
</template>

<script>

export default{
    data: function(){
      return{
        a:1,
      }
    },
    mounted: function(){
    	this.start();
    },
    methods:{
    	start: function(){
    		this.a =  this.a + 1;
    		setTimeout(this.start,1000);
    	}
    },
    watch:{
    	a: function(){
    		console.log(this.a);
    	}
    }


};
</script>