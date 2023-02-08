<h1 align="center">Request</h1>

<p align="center">

<img src="https://img.shields.io/badge/Made%20by-Ogabek-yellow" >

<img src="https://img.shields.io/badge/Methods-request-red">

<img src="https://img.shields.io/badge/Axios-request-red">

<img src="https://img.shields.io/badge/fetch-request-red">

<img src="https://img.shields.io/badge/Learn-Javascript-black">

</p>

---

<center> <h3>API</h3></center>

`«Application Programming Interface»`

<img src="https://hot-hatch.ru/800/600/https/www2.thebigbox.id/wp-content/uploads/2019/08/overview.png">

---

<p align="center" style="font-size:30px;font-weight:900">API VS REST API</p>

> `API is a general term that means "application programming interface".`

>`Rest API это конкретный API, под названием REST, описывающий протокол взаимодействия с веб сервисом.`

---

### REST API

<img src="https://s.7learn.com/uploads/2020/02/rest_api.jpg">

---

<p align="center" style="font-size:30px;color:green;font-weight:900">Fetch()</p>

>` The Fetch API provides a JavaScript interface for working with HTTP requests and responses. It also provides a global fetch()en US) method that makes it easy and logical to get resources over the asynchronous network `

#### GET

```JS
const getUsers = async ( ) =>{
try{
const response = await fetch("");
const
data = await response.json
console.log(data);
}
catch(error){
console.log(error)
}
}
```

#### POST

```JS
const postUser = async (user) =>{
    try {
        const response = await fetch("",
        {
            method: "POST",
            headers: {
                accept: "application/json",
                "Content-Type": "application/json",
                },
                body: JSON.stringify(user),
        });
    } catch (error) {
        console.log(error);
    }
}
```

#### PUT

```JS
const putUser = async (id,edituser) =>{
    try {
        const response = await fetch("",
        {
            method: "PUT",
            headers: {
                accept: "application/json",
                "Content-Type": "application/json",
                },
                body: JSON.stringify(edituser),
        });
    } catch (error) {
        console.log(error);
    }
}
```

#### DELETE

```JS
const deleteUser = async (id) =>{
    try {
        const response = await fetch("",
        {
            method: "DELETE",
        });
    } catch (error) {
        console.log(error);
    }
}
```

<p align="center" style="font-size:40px;color:blue;font-weight:900">axios</p>

>`Axios is a simple promise based HTTP client for the browser and node.js. Axios provides a simple to use library in a small package with a very extensible interface.`

Using unpkg CDN:

`<script src="https://unpkg.com/axios/dist/axios.min.js"></script>`

#### GET

```JS
const getUsers = async ( ) =>{
    try{
        const {data}= await axios.get('')
    } catch(error){
        console.log(error)
    }
}
```

#### POST

```JS
const postUser = async (user) =>{
    try {
        const {data}= await axios.post('',user)
    } catch (error) {
        console.log(error);
    }
}
```

#### PUT

```JS
const putUser = async (id,edituser) =>{
    try {
        const {data}= await axios.put(`url/${id}`,user)
    } catch (error) {
        console.log(error);
    }
}
```

#### DELETE

```JS
const deleteUser = async (id) =>{
    try {
        const {data}= await axios.delete(`url/${id}`)
    } catch (error) {
        console.log(error);
    }
}
```
