<html>
<form>
    <input type="text" value="Enter Your Nickname" id="nameBox">
    <input type="button" value="Go!" id="submit" onClick="putCookie">
<form>


<script>
    var today = new Date();
    var expiry = new Date(today.getTime() + 30 * 24 * 3600 * 1000); // plus 30 days

    function setCookie(name, value){
        document.cookie=name + "=" + escape(value) + "; path=/; expires=" + expiry.toGMTString();
    }
    //this should set the UserName cookie to the proper value;
    function storeValues(form){
        setCookie("userName", form.submit.value);
        return true;
    }

</script>
</body>
</html>
