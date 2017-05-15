<template>
    <div class="itemSub">
        <div>
            <slot name="title"></slot>
            <i class="el-icon-arrow-down" v-if="length>1"></i>
        </div>
        <ul>
            <slot></slot>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'sideBarSub',
    props: ['length']
}
</script>

<style lang="sass">
    .itemSub{
        div{
            padding-left:20px;
            cursor:pointer;
            &:hover{
                background-color:rgba(255,255,255,0.1)
            }
        }
        i{
            float:right;
            margin:13px 20px 0 0;
        }
        ul{
            li{
                padding-left:50px;
                cursor:pointer;
                &:hover{
                    background-color:rgba(255,255,255,0.1)
                }
            }
        }
    } 
</style>

