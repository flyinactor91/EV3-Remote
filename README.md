EV3-Remote
===

2013-12-03

Michael duPont - flyinactor91.com

Controller-robot system for the Lego Mindstorms EV3 running Lejos

Lejos 0.4.0-alpha running on EV3

The default setup is a Left (A) and Right (B) motor with a third motor or servo (C)

This code does not have any sensors

---

Available Commands:

	Motors
		Forward: 	F distance<int> (serial<def=Y /N>)
		Backward: 	B distance<int> (serial<def=Y /N>)
		Left:		L degree<int> (serial< def=Y /N>)
		Right:		R degree<int> (serial< def=Y /N>)
		Servo:		S degree<int +/->
		Motor Speed:	MS motor<M/S> speed<int> ##Main (A and B) / Servo (C)
	Sounds
		Volume:		VOL percent<int 0-100> ##Buzzer/TONE volume > 8%
		Tone:		TONE freq-Hz<int> duration-ms<int>
		Beep:		BEEP pattern<int 1-5>
		Song:		WAV song<*.wav> #Song.wav location
	Utils
		Pause:		P duration-ms<int>
		LED Disp:	LED pattern<int 0-9>
		Battery:	BAT ##Returns the battery level
		Quit:		QUIT

Commands separated by ' ; '

Receivers separated by ' | '

Command structure:

	receiver #1 <int IP index in 'host'> : command #1 ; command #2 ; (etc) | receiver #2 (etc)

Example:

	0 : F 1000 N ; LED 3 | 1 : WAV hello.wav

Notes:

	LED patterns:
		0 = Off , 1 = Green , 2 = Red , 3 = Orange
		4-6 = Even pulses , 7-9 Heartbeat pulses
	Beep patterns:
		1 = beep , 2 = two beeps , 3 = buzzer
		4 = ascending beeps , 5 = descending beeps
	WAV files:
		Refer to Notes file for how to properly format the *.wav file
