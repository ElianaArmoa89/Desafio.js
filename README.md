const jugadorUno = {
    nombre: "Marce",
    habilidades: {
      ataque: 70,
      velocidad: 30,
      vida: 60,
      magia: 120,
    },
    articulos: ["espada", "escudo", "varita"],
  };
  
  const jugadorDos = {
    nombre: "Flor",
    habilidades: {
      ataque: 73,
      velocidad: 30,
      vida: 80,
      magia: 100,
    },
    articulos: ["escudo", "varita", "capa", "pocion"],
  };
  
  let contadorPuntosJug1 = 0;
  let contadorPuntosJug2 = 0;
  
  
  if (jugadorUno.habilidades.ataque > jugadorDos.habilidades.ataque) {
    contadorPuntosJug1++;
  } else if (jugadorUno.habilidades.ataque < jugadorDos.habilidades.ataque) {
    contadorPuntosJug2++;
  }
  
  if (jugadorUno.habilidades.velocidad > jugadorDos.habilidades.velocidad) {
    contadorPuntosJug1++;
  } else if (jugadorUno.habilidades.velocidad < jugadorDos.habilidades.velocidad) {
    contadorPuntosJug2++;
  }
  
  if (jugadorUno.habilidades.vida > jugadorDos.habilidades.vida) {
    contadorPuntosJug1++;
  } else if (jugadorUno.habilidades.vida < jugadorDos.habilidades.vida) {
    contadorPuntosJug2++;
  }
  
  if (jugadorUno.habilidades.magia > jugadorDos.habilidades.magia) {
    contadorPuntosJug1++;
  } else if (jugadorUno.habilidades.magia < jugadorDos.habilidades.magia) {
    contadorPuntosJug2++;
  }
  
  if (jugadorUno.articulos.length > jugadorDos.articulos.length) {
    contadorPuntosJug1++;
  } else if (jugadorUno.articulos.length < jugadorDos.articulos.length) {
    contadorPuntosJug2++;
  }
  
  
  let ganador;
  if (contadorPuntosJug1 > contadorPuntosJug2) {
    ganador = jugadorUno.nombre;
  } else if (contadorPuntosJug1 < contadorPuntosJug2) {
    ganador = jugadorDos.nombre;
  } else {
    ganador = "Empate";
  }
    
  
  let resultado = {
    [jugadorUno.nombre]: contadorPuntosJug1,
    [jugadorDos.nombre]: contadorPuntosJug2,
    ganador: ganador
  };
  
  console.log(resultado.ganador);
  
