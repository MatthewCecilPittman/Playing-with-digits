# Playing-with-digits
/*we want to find a positive integer k, 
if it exists, such as the sum of the digits
 of n taken to the successive powers of p is
 equal to k * n.*/
function digPow(n, p){
var sum = 0;
var myArray = [];
var holder = n;
for (var i = n.toString().length-1; i >=0;i--){
myArray[i] = holder % 10;
holder = Math.trunc(holder/10);
myArray[i] = Math.pow(myArray[i], p+i);
sum += myArray[i];
}
if(sum % n == 0){
return sum/n;
} else{
return -1;
}
}
Test.assertEquals(digPow(89, 1) /*should return 1*/
Test.assertEquals(digPow(92, 1)/*should return -1*/
Test.assertEquals(digPow(46288, 3) /*should return 51*/
Test.assertEquals(digPow(45526652532562,3) /* should return -1*/
