@echo off
@color A
echo Hola, bienvenido a la calculadora
:inicio
echo que desea calcular?
echo (1)-Sumar
echo (2)-Restar
echo (3)-Multiplicar
echo (4)-Dividir
echo (5)-Contar
echo (6)-Secreto
echo (0)-Salir
set /p accion=
if %accion%==1 goto suma
if %accion%==2 goto resta
if %accion%==3 goto multi
if %accion%==4 goto dividir
if %accion%==5 goto contar
if %accion%==6 goto secreto
if %accion%==0 goto salir

:suma
echo que numero desea sumar
set /p num1=
echo cuanto sumara
set /p num2=
set /a res=%num1% + %num2%
echo resultado = %res%
echo volviendo al inicio
timeout 5
goto inicio

:resta
echo que numero desea restar
set /p num1=
echo cuanto restara
set /p num2=
set /a res=%num1% - %num2%
echo resultado = %res%
echo volviendo al inicio
timeout 5
goto inicio

:multi
echo cuanto desea multiplicar
set /p res=
:rep
echo por cuanto desea multiplicarlo
set /p num2=
set /a res=%res% * %num2%
echo el resultado es = %res%
echo desea multiplicar este numero?
echo (1)-Si
echo (2)-No
set /p sino=
if %sino%==1 goto rep
echo volviendo al inicio
timeout 5
goto inicio

:dividir
echo cuanto desea dividir
set /p num1=
echo por cuanto lo dividira
set /p num2=
set /a res=%num1% / %num2%
echo el resultado de la division es = %res%
echo volviendo al inicio
timeout 5
goto inicio

:contar
echo cuantos segundos desea contar
set /p loopcount=
echo segundo %loopcount%
:loop
timeout 1
set /a loopcount=loopcount-1
echo segundo %loopcount%
if %loopcount%==0 goto termino
goto loop

:termino
echo la cuenta ha terminado
echo volviendo al menu
timeout 5
goto inicio

:secreto
start https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRtOXXL7-I8jQkjF9uHqWuUbEy39m9teacBGg&s
:salir
echo cerrando programa
timeout 5