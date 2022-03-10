const obj1 = { x: 20, y: 30 };

function cloneDeep(obj) {
    obj = {...obj1}
    return obj
}
const obj2 = cloneDeep(obj1)
obj2.x = 10
console.log(obj1, obj2);


//EX 2

const macbooks = ['macbook2015', { model: 'macbook2014' }, 'macbook2017'];
const apples = [...macbooks];
apples[0] = 'air';
apples[1].model = 'm1';

console.log(macbooks)
console.log(apples)
// Kết quả của macbooks và apples là gì? Giải thích

// kết quả macbooks là ['macbook2015', { model: 'macbook2014' }, 'macbook2017'];
// kết quả apples là ['air', { model: 'm1' }, 'macbook2017'];

//lý do: vì đã được spread operator 


//EX 3
var text = 'outside';
function show() {
  console.log(text) //1
  var text = 'inside';
}

//Kết quả ra undefined vì trong function có khai báo thêm 1 biến var text nữa => biến text chưa được gán value


//EX 4

// let arr = [1, 2, 3, 4, 5, 6, 7];

// alert( arr.filter(inBetween(3, 6)) ); // 3,4,5,6

// alert( arr.filter(inArray([1, 2, 10])) ); // 1,2

//EX 5

// function Counter() {
//     let count = 0;
  
//     this.up = function() {
//       return ++count;
//     };
//     this.down = function() {
//       return --count;
//     };
//   }
  
//   let counter = new Counter();
  
//   alert( counter.up() ); // ?
//   alert( counter.up() ); // ?
//   alert( counter.down() ); // ?

  //kết quả ra 1 - 2 - 1 vì trong function Counter có 2 function con vì vậy khi gọi cuonter.up() up tức là function trả về biến count += 1 và ngược lại
  
  // EX 6

  console.log("hello");

setTimeout(() => console.log("world"), 0);

console.log("hi");

//kết quả theo thứ tự là "hello" - "hi" - "world" vì setTimeout dù để 0 giây nhưng vẫn phải mất 1 khoảng thời gian để chạy callBack ngược lại 