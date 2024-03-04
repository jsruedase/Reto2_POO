# Reto2_POO

classDiagram
  class Transmilenio {
    - estaciones
    - buses
    - mapas
    + agregarEstacion()
    + agregarBus()

  }

  class Estacion {
    - nombre
    - ubicacion
    - troncal
    + obtenerNombre()
    + obtenerUbicacion()
    + obtenerTroncal()
  }

  class Bus {
    - numero
    - capacidad
    - conductor
    + obtenerNumero()
    + obtenerCapacidad()
    + obtenerConductor()
  }

  class Ruta {
    - origen
    - destino
    - buses
    + agregarBus()
    + obtenerOrigen()
    + obtenerDestino()
    + obtenerBuses()
  }

  class Transmicable {
    - origen = "Portal Tunal"
    - destino = "Mirador del Paraíso"
    + circularCabinas()
    + detenerCabinas()
    + llamarMantenimiento()
  }

  class CabinaTransmicable{
    - numero_cabina
    - tiempo_circulando
    + abordar()
    + abrirVentana()
    + presionarBotonEmergencia()
    + obtenerNumeroCabina()
  }


  class Funcionario {
    - nombre
    - estacion_asignada
    - jornada
    + obtenerNombre()
    + vigilarTorniquete()
    + sacarHabitanteCalle()
    + llamarPolicia()
  }


  Transmilenio --> Estacion
  Transmilenio --> Funcionario
  Transmilenio --> Transmicable
  Transmilenio --> Ruta

  Ruta --> Bus
  Transmicable --> CabinaTransmicable
