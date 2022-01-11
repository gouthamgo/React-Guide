# Login Page

- onCick, onChnage, onSubmit

- useState()-React Hook

- object destructuring
```
import React,{useState} from 'react'


const App = () => {

  const[data,setData]= useState({
    username:'',
    password:''
  })

  const{username, password} = data;
  const changeHandler = e => {
    setData({...data,[e.target.name]:[e.target.value]})
  }

  const submitHandler = e=> {
    e.preventDefault();
    console.log(data)
  }

  return (
    <div>
    <form onSubmit={submitHandler}>
    <input type="text" name="username" value={username} onChange={changeHandler}/>
    <br/>
    <input type="password" name="password" value={password}
      onChange={changeHandler}
    />
      

      <input type="submit" name="submit"/>

      </form>
    </div>
  )
}

export default App
```
