
创建对象的方式 name age job
工厂模式
function createPerson(name, age, job) {
    var o = new Object();
    o.name = name;
    o.age = age;
    o.job = job;
    o,sayName = function() {
        alert(this.name)
    }
    return 0
}
函数createPerson根据接收的参数来构建一个包含所有必要信息的person对象，可以无数次的调用此函数，解决了创建多个函数的问题，没有解决对象识别的问题

构造函数模式
