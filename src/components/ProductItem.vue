<template>
   <div>
    <figure>
        <img :src="item.image" :alt="item.name" />
        <figcaption>
            <dl>
                <dt>{{item.name}}</dt>
                <dd>{{item.description}}</dd>
                <dd>레벌</dd>
                <dd>{{item.price}}</dd>
            </dl>
        </figcaption>
    </figure>
    <p><button @click="$emit('addToCart',item)">+</button></p>
   </div>
</template>
<script>
export default {
    props:{
        item:{type:Object}
    },
    emits:['addToCart']
}
</script>
<style scoped>
figure{
    width:800px;
    display:flex;
    flex-wrap:wrap;
    justify-content: space-between;
    align-content: flex-start;
}
figure>img{
    width:150px;
}
figure>figcaption{
    width:500px;
    /* background-color:pink; */
}
figure dl{
    padding:0 20px;
}
figure dl>dt{
    font-size:1.5em;
    padding:8px 0;
    border-bottom:1px dotted #666;
}
figure dl>dd{
    padding:5px 0;
    border-bottom:1px dotted #666;
}
figure dl>dd:last-child{
    border-bottom:none;
}
figure dl>dd:nth-of-type(2){
    padding:10px 0;
    text-align:right;
}
figure dl>dd>span{
    color:#fff;
    line-height:35px;
    padding:0 10px;
    border-radius:4px;
    display:inline-block;
}
figure dl>dd>span.blue{
    background-color:#0f2561;
}
figure dl>dd>span.green{
    background-color:#228866;
}
figure dl>dd>span.orange{
    background-color:#b6402b;
}
p{
    width:100px;
    display:flex;
    justify-content: center;
    align-items: center;
}
</style>