###############################################################################
# Makefile for project 
###############################################################################

## General options
PROJECT = 
MCU = 80C31
COMPILER = "ASEM-51 (Proteus)"
TARGET = Debug
SHELL = C:\WINDOWS\system32\cmd.exe

## Tools general options

## Processing Tools
ASM=asem.exe
DDX=ASEMDDX.EXE
#  D:/学习/计组/myself 课设/19317129-潘政伍/80C31/Debug/Debug.HEX: TOOL=ASM
#  Post: $(DDX) $(DDXFLAGS) Debug.lst
#     D:/学习/计组/myself 课设/19317129-潘政伍/cm3/cm3.asm

# Build tree:
all:	Debug

Debug:	Debug.HEX

Debug.HEX:	../../cm3/cm3.asm 
	$(ASM) "..\..\cm3\cm3.asm" "Debug.HEX" Debug.lst $(ASMFLAGS)  /INCLUDES:"..\..\..\..\..\..\Proteus 8 Professional\Tools\ASEM51"
	$(DDX) $(DDXFLAGS) Debug.lst

# tidy - delete all temporary files which are not involved in the target generation
tidy:
	rm -rf Debug.lst

# cleanup - delete all generated files
clean:	tidy
	rm -rf Debug.HEX
	rm -rf Debug.SDI
