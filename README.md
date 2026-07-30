# Lin-s-NES-Audio-Engine
An Audio engine I made for the NES, using CC65 and it's hl macro set, it totals 863 bytes in size, and uses 144 bytes of WRAM, and 18 bytes of the Zero Page,

Anyone is free to use it, but as a few additional notes for the format

The engine relies on the following variables, the given addresses do NOT need to be exact, but it is recommended to keep their positions similar.
They DO need to be set in an $YYX0 and $YYX1, due to how the engine works.
While not nessecary, I do HIGHLY recommend to keep the zChn_Data pointers IN the Zero page, else the engine will be a bit larger and run a bit slower.

//____ZERO PAGE____//
zAPU_Sound				:= $000C
zAPU_Music				:= $000D

zChn_Data_Lo			:= $00D0
zChn_Data_Hi			:= $00D1


//____WORK RAM____//
wAudio_Timer			:= $0300
wAudio_Loops			:= $0301

wAudio_Volume			:= $0310
wAudio_Duty				:= $0311

wAudio_Sweep			:= $0320    *UNUSED*
wAudio_Delay			:= $0321

wAudio_Vibrato_Def		:= $0330
wAudio_Vibrato_Length	:= $0331
wAudio_Vibrato_Lo		:= $0340
wAudio_Vibrato_Hi		:= $0341
wAudio_Vibrato_Timer	:= $0350

wAudio_Tremolo_Def		:= $0351
wAudio_Tremolo_Length	:= $0360
wAudio_Tremolo_Timer	:= $0361
wAudio_Tremolo_Shift	:= $0370

wAudio_Period_Hi_Old	:= $0371

wAudio_Period_Index		:= $0380
wAudio_Period_Base		:= $0381

