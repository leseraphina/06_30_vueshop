<template>
    <header>
        <h3>제품카테고리</h3>
        <dl>
            <dt>구매상품 총 </dt>
            <dd>????원</dd>
            <dd>
                <button>장바구니 보기 ???개</button>
                <ul>
                    <li>
                        <span><img src="" alt="" /></span>
                        <span>이름 : 가격 원</span>
                    </li>
                </ul>
            </dd>
        </dl>
    </header>
</template>
<script>
export default {
    
}
</script>
<style scoped>
header{
    display:flex;
    justify-content: flex-end;
    align-items: center;
    position:relative;
    padding:10px 20px;
    border-bottom:1px solid #666;
}
header>dl{
    display:flex;
    justify-content: flex-end;
    align-items: center;
}
header>dl>dd>ul{
    position:absolute;
    right:0; top:45px;
    z-index: 100;
    padding:5px 10px;
    border:1px solid #666;
    background-color:#fff;
}
header>dl>dd>ul>li{
    border-bottom:1px dotted #666;
    padding:10px 0;
}
header>dl>dd>ul>li:last-child{
    border-bottom:none;
}
</style>