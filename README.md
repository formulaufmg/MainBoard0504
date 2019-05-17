# C�digo Main Board

C�digo da placa principal do sistema de aquisi��o de dados.
Modo de transmiss�o para telemetria:
0 - String
1 - Bytes 
Frequ�ncia de comunica��o pela CAN: 1MBits/s
Frequ�ncia de envio pela telemetria: 
1� pacote - 40Hz
2� pacote - 20Hz
3� pacote - 10Hz
4� pacote - 40Hz 
Tempo entre cada interrup��o do Timer para envio na telemetria : 25 ms

#|ordem\pacote|		1�		|		2�		|		3�		|
|	  1�	 |		a_x		|	   OILP		|	   ECT		|
|	  2�	 |		a_y		|	  FUELP		|	   BAT		|
|	  3�	 |		a_z		|	   TPS		|	   VENT		|
|	  4�	 |	 SPEEDFR	|	 PFREIOT	|	TEMPPDU		|
|	  5�	 |	 SPARKC		|	 PFREIOD	|	TEMPBREAK_1	|
|	  6�	 |		SUSP	|	 POSVOL		|	TEMPBREAK_2	|
|	  7�	 |	TIMERCOUNT	|	 BEACON		|	TIMERCOUNT	|
|	  8�	 |				|	CORRENTE	|				|
|	  9�	 |				|	TIMERCOUNT	|				|
OBS: Deve-se lembrar que dependendo da forma que � transmitido, no pacote pode conter o numero do pacote e a quantidade de dados.