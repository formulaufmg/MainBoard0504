# Código Main Board

Código da placa principal do sistema de aquisição de dados.
Modo de transmissão para telemetria:
0 - String
1 - Bytes 
Frequência de comunicação pela CAN: 1MBits/s
Frequência de envio pela telemetria: 
1º pacote - 40Hz
2º pacote - 20Hz
3º pacote - 10Hz
4º pacote - 40Hz 
Tempo entre cada interrupção do Timer para envio na telemetria : 25 ms

#|ordem\pacote|		1º		|		2º		|		3º		|
|	  1º	 |		a_x		|	   OILP		|	   ECT		|
|	  2º	 |		a_y		|	  FUELP		|	   BAT		|
|	  3º	 |		a_z		|	   TPS		|	   VENT		|
|	  4º	 |	 SPEEDFR	|	 PFREIOT	|	TEMPPDU		|
|	  5º	 |	 SPARKC		|	 PFREIOD	|	TEMPBREAK_1	|
|	  6º	 |		SUSP	|	 POSVOL		|	TEMPBREAK_2	|
|	  7º	 |	TIMERCOUNT	|	 BEACON		|	TIMERCOUNT	|
|	  8º	 |				|	CORRENTE	|				|
|	  9º	 |				|	TIMERCOUNT	|				|
OBS: Deve-se lembrar que dependendo da forma que é transmitido, no pacote pode conter o numero do pacote e a quantidade de dados.