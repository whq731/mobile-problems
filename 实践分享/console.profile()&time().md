function createArray1(){
    for(var i=0;i<100000;i++){
        var arr = [];
    }
}
function createArray2(){
    for(var i=0;i<100000;i++){
        var arr = new Array;
    }
}
console.profile('a');
createArray1();
console.profileEnd('a');
 
console.profile('b');
createArray2();
console.profileEnd('b');

来自 <http://www.cnblogs.com/zhenn/archive/2011/02/20/1959186.html> 

测试占用cpu

console.time('a');
createArray1();
console.timeEnd('a');

测试占用时间
来自 <http://www.cnblogs.com/zhenn/archive/2011/02/20/1959186.html> 


