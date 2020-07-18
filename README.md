
Algoritmo

  Clase Prestamo 
   1.  Declarar
        // se declaran datos o atributos con visibilidad protegido
        # nombresBeneficiario: Cadena
        # sueldoBeneficiario: Real
        # montoCredito: Real
        # tiempoCredito: Entero

//  Métodos establecer y calcular para los datos o atributos de la clase
    2.  Método establecerNombresBeneficiario(nom: Cadena)
        a.  nombresBeneficiario = nom
        b.  Fin Método establecerNombresBeneficiario
   
3.  Método establecerSueldoBeneficiario(suel: Real)
        a.  sueldoBeneficiario = suel
        b.  Fin Método establecerSueldoBeneficiario 

    4.  Método establecerMontoCredito(mon: Real)
        a.  montoCredito = mont
        b.  Fin Método establecerMontoCredito 

    5.  Método establecerTiempoCredito(tiem: Entero)
        a.  tiempoCredito = tiem
        b.  Fin Método establecerTiempoCredito

    //  Métodos obtener para los datos o atributos de la clase
    6.  Método obtenerNombresBeneficiario() : Cadena
        a.  return nombresBeneficiario 
        b.  Fin Método obtenernombresBeneficiario 

    7.  Método obtenerSueldoBeneficiario() : Real
        a.  return sueldoBeneficiario 
        b.  Fin Método obtenerSueldoBeneficiario

    8. Método obtenerMontoCredito() : Real
        a.  return montoCredito
        b.  Fin Método obtenerMontoCredito

    9.  Método obtenerTiempoCredito() : Entero
        a.  return tiempoCredito
        b.  Fin Método obtenerTiempoCredito

  Fin Clase Prestamo
  
  Clase PrestamoVehiculo hereda de Prestamo
    1.  Declarar
        tipoVehiculo: Cadena 
        marcaVehiculo: Cadena 

   //  Métodos establecer y calcular para los datos o atributos de la clase
    2.  Método establecerTipoVehiculo(tipo: Cadena)
        a.  tipoVehiculo = tipo
        b.  Fin Método establecerTipoVehiculo

   3.  Método establecerMarcaVehiculo(marca: Cadena)
        a.  marcaVehiculo = Marca
        b.  Fin Método establecerMarcaVehiculo

   //  Métodos obtener para los datos o atributos de la clase
    5. Método obtenerTipoVehiculo() : Cadena
        a.  return tipoVehiculo 
        b.  Fin Método obtenerTipoVehiculo
        
   6. Método obtenerMarcaVehiculo() : Cadena
        a.  return marcaVehiculo
        b.  Fin Método obtenerMarcaVehiculo

  Fin Clase PrestamoVehiculo
  
  
  Clase EjecutaPrestamo
    1.  Método principal()
        // Se declaran variables
        a.  Declarar Variables
            nombresBenef: Cadena 
            sueldoBenef: Real
            montoCred: Real
            tiempoCred: Entero
            tipoVeh: Cadena
            marcaVeh: Cadena
            tipoBeneficiario: Entero
            continuar: Carácter
     
     b.  // Incio ciclo repetitivo
            do 
            // Se impreme mensaje en pantalla para solicitar
            // el tipo de beneficiario que se desea ingresar
            1. Imprimir "Tipo de Beneficiario a ingresar
               1. PrestamoVehiculo
            // se captura el valor ingresado por el usuario en 
            // la variable tipoBeneficiario
            2. Leer tipoBeneficiario
            // Solicitar el ingreso de valores para las variables
            3. Solicitar nombresBenef, sueldoBenef, montoCred, tiempoCred
            4. Leer nombresBenef, sueldoBenef, montoCred, tiempoCred
            5. if tipoBeneficiario == 1 then
              a.  // Declarar,crear e iniciar objeto tipo PrestamoVehiculo
                  PrestamoVehiculo prestamoV = new PrestamoVehiculo()
              b.  // Solicitar ingreso de valores para variables 
                  // tipo de vehiculo, marca de vehiculo
                  Solicitar tipoVeh, marcaVeh
              c.  Leer tipoVeh, marcaVeh

              d.  // se hace uso de los métodos establecer para asignar valores
                  // a los datos (atributos) del objeto
                  Establecer:  
                        prestamoV.establecerNombresBeneficiario(nombresBenef),
                        prestamoV.establecerSueldoBeneficiario(sueldoBenef),
                        prestamoV.establecerMontoCredito(montoCred),
                        prestamoV.establecerTiempoCredito(tiempoCred),
                        prestamoV.establecerTipoVehiculo(tipoVeh),
                        prestamoV.establecerMarcaVehiculo(marcaVeh)

              e.  // Luego que se ha ingresado los datos, se hace uso del método
                  // calcular Valor Prestamo para el objeto tipo
                  // ValorPrestamo
                  Calcular: prestamoV.calcularValorPrestamo()

              f.  // se hace uso de los métodos obtener del objeto para presentar
                  // los valores que se necesite en pantalla
                  Imprimir:
                      prestamoV.obtenerNombresBeneficiario(),
                      prestamoV.obtenerSueldoBeneficiario(),
                      prestamoV.obtenerMontoCredito()
                      prestamoV.obtenerTiempoCredito()
                      prestamoV.obtenerValorPrestamo()
           
           6. endif
            7. // Se pregunta si se desea ingresar más beneficiarios
               Imprimir "Desea ingresar más beneficarios. Digite la letra S para
               continuar o digite la letra N para salir del proceso"
            8. // se captura el valor ingresado por el usuario para la variable
               // carácter 
               Leer continuar
        // se pregunta si el valor continuar es igual al valor "S", se sigue en 
        // ciclo repetitivo; si el valor es distinto de "S", se sale del ciclo
        // repetitivo
        c.  while continuar == "S" 
        d.  Fin Método principal
    
  Fin Clase EjecutaBeneficiarios  
Fin 
