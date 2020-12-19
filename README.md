<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Pruebas</title>
    
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
    <link rel="stylesheet" href="css/estilo.css">
    <script src="https://kit.fontawesome.com/23fb3fd4c4.js" crossorigin="anonymous"></script>
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Sansita+Swashed&display=swap" rel="stylesheet">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>
    
    <?php session_start()?>
   <nav class="navbar navbar-expand-lg navbar-dark" style="background-color:  #127e37">
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item active">
                    <a class="nav-link" href="#">Forean's <span class="sr-only"></span></a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link" href="php/Acerca-de.php">Acerca de</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link" href="php/contactanos.php">Contáctanos</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link" href="php/ayuda.php">Ayuda</a>
                </li>
            </ul>
            <li class="navbar-nav dropdown">
                <a class="nav-link dropdown-toggle" href="index.php" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                  Mi cuenta
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                    <?php
                        if(!empty($_SESSION["usuario"])){
                            echo"<h6 class='dropdown-item'>".$_SESSION["usuario"]."</h6>";
                            echo"<a class='dropdown-item' href='PHP/logout.php'>Cerrar sesión</a>";
                        }else{?>
                            <form class="form" role="form" action="PHP/login.php" method="post">
                                <div class="form-group">
                                    <input name="usuario" id="emailInput" placeholder="Email" class="form-control form-control-sm" type="text" required="">
                                </div>
                                <div class="form-group">
                                    <input name="palabra_secreta" id="passwordInput" placeholder="Password" class="form-control form-control-sm" type="password" required="">
                                </div>
                                <div class="form-group">
                                    <button type="submit" class="btn btn-primary btn-block">Iniciar sesión</button>
                                </div>
                                <input type="hidden" name="page" value='../index.php'> 
                            </form>
                            <a class="dropdown-item" href="PHP/registro.php">Crear cuenta</a><?php
                        }
                    ?>
                </div>
            </li>
            <i class="fas fa-shopping-cart" style="color: white; font-size: 22px"></i>
            <i >1<?php //No. Productos ?></i>     
    </div>
</nav>
 

<div>
    <div class="recom">
       <h3>Nuestra recomendación.</h3>
       <br>
        <div>
           <img src="images/Comida-1.jpg" alt="" id="imag">
       </div>
       <div>
            <img src="images/Comida-2.jpg" alt="" id="imag">   
       </div>
       <div>
           <img src="images/Comida-3.jpg" alt="" id="imag">
       </div>
       <div>
           
       </div>
    </div>
    
    <div class="combo">
        <h3>Elije Un combo</h3>
    </div>
  
</div>
     
        
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
<footer>
    <div class="foot">
        <p>Forean's / Derechos reservados 2020</p>
        <div>
            <a href=""></a>
            <a href=""></a>
        </div>
    </div>
</footer>    
    
    
    
    
    
    
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
            
</body>
</html>
