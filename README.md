
**Solution 1:**
```javascript
var object={
    name:'John',
    age:35,
    fun:function f1(){
        return this.name + ' is '+ this.age + ' years old.';
    }
};
```
**`this`** can be used in different contexts in javascript. One of it's common use being in a `method`, where it refers to the object itself (as shown in the code snippet). In a `function`, it refers to the global object, which is the window object. The value of **`this`** in a function can be bound to a particular user-defined object using the `call()` and `apply()`. The behaviour of **`this`** varies in the `strict` mode, in which it remains *undefined* if the execution context does not explicitly define it.

**Solution 2:**
```java
public void synchronized function(){
    System.out.println("This is a test code snippet\n");
}
```
Every Java object is assigned a `monitor` and a `mutex` semaphore, which restricts the access to the object or the method (those which constitite the critical section of the code) and ensures that a mutually exlusive environment is gauranteed among concurrently executing threads. A thread needs to gain access to the mutex lock to execute a method or utilize an object. Other threads need to wait in the queue for the current thread to finish its execution and release the lock for it to gain access. The **`synchronized`** keyword is used to achive this mechanism.

**Solution 3:**
### Steps to build a website:
**Step 1 : Name it : Domain name**
Identify a `domain name` which is suitable for the website. It must be short enough for the users to remember it and also reflect the purpose of the website.

**Step 2 : Hosting**
Choose a web hosting for your website. Some of the popularly used web hosts being `BlueHost`, `GoDaddy`, `A2Hosting` etc.

**Step 3 : Create it**
Coding a website can be listed as a 5-step process internally:

##### Choose an appropriate web framework to build your website.
Depending on the application being developed, the framework must be chosen. As in, `Flask` is apt for small-scale applications whereas `Pyramid` and `Django` are best for large applications.

##### Content Development: 
Design the UI elements of the website using HTML. HTML defines the `structure` and the `layout` of the web document by using tags and attributes.
```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="style.css" type="text/css">
        <title>About us</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body class='body'>
        <div class="header">
            <div class="header_part1"><img src="symbol.png" alt="symbol here" id="sym"/></div>
            <div class="header_part2">Coder's hub</div>
        </div>
        <div class="div2">
            <a href="about_us.jsp"><input class="button" type="submit" name="tutors" value="Tutors"/>
            </a><input class="button" type="submit" name="courses" value="Courses"/>
        </div>
    </body>
</html>
```

##### Styling: 
Styling UI improves the `presentation` of the site which is essential for a better UX. Unlinking the presentation(style) from the content facilitates `reusing` the style sheets, `easier updates` and also `faster loading` of webpages as once the css file has been downloaded, it can be cached and be applied to subsequent pages.
```css
.div2{
    width: 100%;
    height: 50%;
    display: inline-block;
    padding:30px;
    align-self: center;
}
.button{
    width:80%;
    height:200%;
    font-family: 'Diplomata SC';
    font-size: 200%; 
}
```
##### Animate it : Interactivity
Create and link `Javascript` files to the webpage to perform client-side processing of data which will make the site more `responsive` and reduce server traffic. Similarly,link PHP files for server-side processing of confidential data.
```javascript
function myf1()
    {
        var re=/^[.a-zA-Z0-9]{3,10}$/;
        var c=document.getElementById("demo");
        var a= document.getElementById("txt").value;
        if(!re.test(a))
        {
            c.innerHTML="enter valid name";
            document.getElementById("txt").setAttribute("class","war_msg");
            return false;
        }
        return true;
    }
```
##### Integrate it: 
Binding webpages to the urls(if using flask or Django)
```python
from flask import Flask, render_template
app = Flask(__name__)
@app.route('/')
def main():
    return render_template('index.html')
if __name__ == '__main__':
    app.run(debug=True)
```
**Step 4 : Backend Support**
Create the databases required for the proper functioning of the website. In the case of Django, `Migrations` effectively handle any changes made to schemas unlike the traditional way which demands the developer to manually rebuild all the databases again.

**Step 5 : Host it**
Finally run your server and host your website on the web host.

**Solution 4:**

Prior to the advent of **`JSON`** (Javascript Object Notation), `XML` was the only choice for the developers to exchange data across the web. But it was noticed that the time required to parse XML was considerably more. **`JSON`** was then proposed by `Douglas Crockford` and was derived as a subset of Javascript's object notation. It is to be noted that JSON still allows some unescaped charaters which are not accepted in JavaScript.
Some of its discrete features are:

|Feature|Description|
|---|----|
|Less Verbose|JSON has a more compact style than XML, and it is often more readable. The `lightweight` approach of JSON can make significant improvements in RESTful APIs working with complex systems.|
|Faster|The XML software parsing process can take a long time. One reason for this problem is the DOM manipulation libraries that require more memory to handle large XML files. JSON uses less data overall, so you reduce the cost and increase the parsing speed.|
|Readable|The JSON structure is `straightforward` and `readable`. You have an easier time mapping to domain objects, no matter what programming language you're working with.|
|Structure matches the data|JSON uses a `map` data-structure rather than XML's tree. In some situations, key/value pairs can limit what you can do, but you get a predictable and easy-to-understand data model.|
|JSON Limitation|The limitations in JSON actually end up being one of its biggest benefits. A common line of thought among developers is that XML comes out on top because it supports modeling more objects. However, JSON's limitations simplify the code, add predictability and increase readability.|

Information credits: <https://blog.cloud-elements.com/using-json-over-xml> 

In the context of Python, JSON is handled using the `json` library, using methods like `json.dump()` and `json.dumps()` for serializing data (converting Python to JSON) and `json.load()` and `json.loads()` for deserializing it (converting JSON to Python).
##### Serialization:
|Python|JSON|
|---|---|
|dict|object|
|list,tuple|array|
|str|string|
|float,int,long|number|
|True|true|
|False|false|
|None|null|
##### Deserialization:
|JSON|Python|
|---|---|
|object|dict|
|array|list|
|string|str|
|number(int)|int|
|number(real)|float|
|true|True|
|false|False|
|null|None|
```python
import json
json_data=json.loads(json_string)
print(type(json_data))
print(json_data)
```
The code prints `<class 'dict'>` and `{'student': {'name': 'Feymann', 'age': '66', 'books': [{'physics': 'physics book', 'chemistry': 'chemistry book'}]}}` as the output
