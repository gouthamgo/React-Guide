# OnSubmit- Event Hnadler in ReactJs



<img width="683" alt="j17-onsubmit" src="https://user-images.githubusercontent.com/24316133/148757149-b5348c89-03cb-448d-9873-0762d863d781.png">




```
import React,{useState} from 'react'
import './App.css';


const App = () => {

  const[data, setData] = useState({
    username:'',
    password:'',
  })
 
  const{username,password} =data;
  const onChange= e => {
    setData({...data,[e.target.name]:[e.target.value]})
  }
  const submitHandler = e => {
  e.preventDefault();
  console.log(data);
  }
   
  return (
    <div className='top'>
   
   <center>
     <form onSubmit={submitHandler}>
       <input type="text" name="username" value={username}
       onChange={onChange} placeholder="Username"/> <br/>

         <input type="text" name="password" value={password}
       onChange={onChange} placeholder='Password'/> <br/>

       <input type="submit" name='submit'/>
     </form>
   </center>
     
    </div>
  )
} 

export default App
 ```
