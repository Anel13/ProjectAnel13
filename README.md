<html>
	<head>
		<title>My site</title>
    <link rel="stylesheet" href="css/bootstrap.css" media="screen" title="no title"/>
    <link rel="stylesheet" href="css/bootstrap.min.css" media="screen" title="no title"/>
    <link rel="stylesheet" href="css/bootstrap-theme.css" media="screen" title="no title"/>
    <link rel="stylesheet" href="css/bootstrap-theme.min.css" media="screen" title="no title"/>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
    <script type="text/javascript" src="js/bootstrap.js"></script>
    <link rel="stylesheet" type="text/css" href="mood.css">
	</head>
    <body style="background-image:url(wide.jpg);background-size:cover; background-attachment: fixed;">
    	
       <div class="col-md-12 col-lg-12 col-sm-12 col-xs-12" style="background-color: rgba(0,0,0,0.5 ); height:150%;">
       <p align="center" style="color:white; font-size:300%; font-variant: small-caps;">Registration</p>
       <hr>
     
    <div class="row" style="margin-right:630px; margin-top:20px;">
        <div class="col-md-3 col-md-offset-6">
            <div class="modal-dialog">
    <div class="modal-content" style="height:600px">
    <div class="modal-body">
      
            <!-- content goes here -->
              <div class="form-group">
                <label for="first_name">First Name</label>
                <input type="text" id="first_name" class="form-control"  placeholder="First Name">
              </div>
              <div class="form-group">
                <label for="last_name">Last Name</label>
                <input  type="text" id="last_name" class="form-control"  placeholder="Last Name">
              </div>
              <div class="form-group">
                <label for="username">Username</label>
                <input  type="text" id="username" class="form-control"  placeholder="Username">
              </div>
              <div class="form-group">
                <label for="password">Password</label>
                <input  type="password" id="password" class="form-control"  placeholder="Password">
              </div>
              <div class="form-group">
                <label for="email">Email</label>
                <input  type="email" id="email" class="form-control"  placeholder="Email">
              </div>
              <p><button type="submit" class="btn btn  -default"  onClick="reg()" style="font-variant: small-caps; background-color:black; border-radius:4px; border-size:1px; border-color: black; width:120px; height: 50px; margin-left:210px; margin-top:80px; font-weight:bold; color:white;">Submit</button>
              <a href="login.php" style=" margin-left:150px; margin-top:0px; font-variant: small-caps; font-weight:bold; color:black;">Log In</a>
              
              <div class="fin" style="color:black; font-variant: small-caps;"></div>
            
            </div>
        </div>
        </div>
  </body>
</html> 
<script type="text/javascript">
  function reg(){
    var first_name = $('#first_name').val();
    var last_name = $('#last_name').val();
    var username = $('#username').val();
    var password = $('#password').val();
    var email = $('#email').val();
    $.ajax({
      type: 'POST',
      url: 'rcod.php',
      data: "first_name="+first_name+"&last_name="+last_name+"&username="+username+"&password="+password+"&email="+email,
      success: function(data){
        if (data=="Success"){
          $('.fin').html("Successfully!");
        }else{
          $('.fin').html(data);
        }
      }
    });
  }
</script>
