

<template>
<div>{{yjx.name}}</div>
<button @click="clic">点击</button>
<HelloWorld></HelloWorld>
</template>

<script setup lang="ts">
import { ref } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

  const message:number = 20;
 type Style = {color:string,height:string};
 const style1:Style = {
  color:'red',
  height:'200px'
 }
 const flag:boolean=true;
 type man ={
  name:String
 }
 interface Person {
  readonly name:string,
  age?:number,
  [test:string]:any,
  fun():string
 }
 let arr:number[] = [123,11]
 let ar1r:Array<number> = [123,11];
  let arr2:Array<Array<number>> = [[23,23],[44,55]]

    const fn2 = function(a:number,b:number = 20):number{
      return a+b;
    }

    interface User{
      name:string,
      age:number
    }
    const fn3 = function(test:User):User{
      return test
    }
    fn3({
      name:'f',
      age:3
    });

    //函数重载  -- 名字相同 参数 返回值 不同
    

 const test1:Person = {
  name:'hhh',
  ff:123,
  fun:function():string{return 'fff'}
 }


 const yjx= ref<man>({name:'yjx'})   
 const list:Array<number> = [1,2,5,4,7];
  const clic = ()=>{
    yjx.value.name = 'hhhhh';
  }



</script>

<style>
  .a{
    color:aqua;
  }
  .b{
    width: auto;
  }
</style>
