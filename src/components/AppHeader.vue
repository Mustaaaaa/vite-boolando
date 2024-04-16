<template>
    <header>
            <nav class="header-bar container">
                <div>
                    <ul class="row gap-5">
                        <li>Donna</li>
                        <li>Uomo</li>
                        <li>Bambini</li>
                    </ul>
                </div>
                <div>
                    <img src="/boolean-logo.png" alt="">
                </div>
                <div >
                    <ul class="icon-header row gap-5"> 
                        <li>&#127900;</li>
                        <li>&#127900;</li>
                        <li>&#127900;</li>
                    </ul>
                </div>
            </nav>
        </header>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
.header-bar{
    display: flex;
    justify-content: space-between;
    line-height: 50px;
    background-color: rgb(255, 115, 0);
    padding: 0 65px;
    color: white;
    align-items: center;
    margin-bottom: 40px;
}
.gap-5{
    gap: 5px;
}
.icon-header{
    font-size: 19px;
}
.header-bar img{
    display: flex;
    max-height: 30px;
}
</style>