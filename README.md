<head>
    <script>
var today = new Date();
  var expiry = new Date(today.getTime() + 30 * 24 * 3600 * 1000); // plus 30 days

  function setCookie(name, value)
  {
    document.cookie=name + "=" + escape(value) + "; path=/; expires=" + expiry.toGMTString();
  }
function putCookie(form)
                //this should set the UserName cookie to the proper value;
  {
   setCookie("userName", form[0].usrname.value);

    return true;
  }

  </script>
</head>
<body>
<form>
 <input type="text" value="Enter Your Nickname" id="nameBox" name='usrname'>
 <input type="button" value="Go!" id="submit" onclick="putCookie(document.getElementsByTagName('form'));">
</form>
</body>
