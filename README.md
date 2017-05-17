<html>
<input type="text" id="userInput"/>
<button onclick="test()">Submit</button>
<script>
function setCookie(cname,cvalue,exdays)
{
var d = new Date();
d.setTime(d.getTime()+(exdays*24*60*60*1000));
var expires = "expires="+d.toGMTString();
document.cookie = cname+"="+cvalue+"; "+expires;
}

function getCookie(cname)
{
var name = cname + "=";
var ca = document.cookie.split(';');
for(var i=0; i<ca.length; i++) 
  {
  var c = ca[i].trim();
  if (c.indexOf(name)==0) return c.substring(name.length,c.length);
  }
return "";
}

function checkCookie()
{
var user=getCookie("username");
if (user!="")
  {
  window.location.href ="emicle1.github.io" 
  }
else 
  {
  if (user!="" && user!=null)
    {
    setCookie("username",user,30);
    }
  }
}
function test()
        {
            var userInput = document.getElementById("userInput").value;
            setCookie("username",userInput,30);
            checkCookie();
        }
</script>
</html>
