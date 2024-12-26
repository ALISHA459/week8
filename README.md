# week 7
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';
import Hook_ControlledButtonState from './Counter';
import EmojeeCounters from  './EmojeeCounters'



const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <Hook_ControlledButtonState />
   < EmojeeCounters pic='Love'/> 
<EmojeeCounters pic='sad'/> 
<EmojeeCounters pic='Like'/> 
  
  </React.StrictMode>,
  document.getElementById('root')
);



// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
import React, { useState ,useEffect} from "react"; 
import Love from './Love.png' 
import sad from './sad.png' 
import Like from './like.png' 
function EmojeeCounter(props){ 
console.log("pic is ",props.pic) 
 
const [pic, setPic]=useState(Love) 
const [count,setCount]=useState(0) 
useEffect(()=>{ 
console.log ("function called",props.pic) 
if (props.pic==="Love") 
  setPic(Love) 
else if   (props.pic==="Like") 
  setPic(Like) 
else if  (props.pic==="sad") 
  setPic(sad) 
}) 
const ClickHandle=() => 
   { 
    setCount(count+1) 
   }  
return ( 
<div className="App"> 
    <p>{props.pic} <span></span> 
    <button onClick={ClickHandle}>{count } 
    <img src={pic} alt=""/> 

    </button> 
</p> 
</div> 
) 
} 
export default EmojeeCounter; 
