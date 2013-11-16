piMotoDriver
============

## Resumen
Este es un sencillo driver que expone una api amigable para ser consumida desde cualquier tipo de aplicación.
Esta construida sobre la plataforma de RaspberryPi usando la librería RPi.GPIO y un placa controlador que diseñamos especialmente para aprovechar al máximo la capacidad de movimiento sin afectar el rendimiento de la Raspi.
Maneja dos motores de continua en ambos sentidos y dos servomotores.

## Ejemplo de uso

	from braianDriver.robot import Robot

	myRobot = Robot()
	myRobot.set_forward()
	myRobot.move(speed=Robot.SPEED_MEDIUM)

	myRobot.set_backward()
	myRobot.move(speed=Robot.SPEED_HIGH)

	myRobot.set_rotate_left()
	myRobot.move(speed=Robot.SPEED_LOW)

	myRobot.set_rotate_right()
	myRobot.move(speed=Robot.SPEED_LOW)

También se puede usar para hacer giros suaves en arco, no solo como si fuera un tanque.

	myRobot.set_forward()
	myRobot.move(arc=Robot.RIGHT_ARC_CLOSE)

Los servos son usados para mover los ejes de, por ejemplo, una cabeza.

	myRobot.head_move_up()
	myRobot.head_move_down()


## Instalacion

	pip install -r requirements.txt

## Next steps

* Ampliar la documentación
* Agregar tests para ampliar los ejemplos de uso
* Agregar parametros de configuracion para limites en el rango de movimiento de los servos.



