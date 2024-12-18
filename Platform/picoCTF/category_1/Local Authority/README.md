# Local Authority [Easy] (by LT 'syreal' Jones) - picoCTF 2022
> <p>Can you get the flag?</p>


We can open the `Network` tab, when we try to log in the page, there is a `secure.js` file. And the username and password is inside:
```javascript
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```


flag: `picoCTF{j5_15_7r4n5p4r3n7_05df90c8}`