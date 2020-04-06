# VR
## Домашна задача 1
Започнав со воведување на 3D објект - `Terrain` околу кој на сите 4 страни додадов `Box Collider` со цел да се оневозможи отстапување на играчот од поставениот терен. 
</br></br>
Потоа на објектот `Main Camera` додадов компонента `Character Controller` каде се подесуваат спецификациите на карактерот и со чија помош му ги доделуваме функционалностите. Следно целиот тој објект го додадов на ново креираниот објект `Player` на кој додадов скрипта `VrLookWalk` која му овозможува на играчот да се движи нанапред со навалување на главата под одреден агол. Ова се прави со помош на вредноста на X во `Rotation` што се наоѓа во `Transform` на `Main Camera`. Така што додека играчот гледа право вредноста на X = 0 а кога ја навалува главата стигнува до вредност 90 што ни го дава опсегот на положби во кои потенцијално може да почне да се движи, но во конкретниов случај аголот на навалување после кој почнува да се движи е 10 (`ToggleAngle`), а брзината со која се движи е 25. 
</br></br>Условите кои треба да се исполнети за да се движи играчот:</br>
`vrCamera.eulerAngles.x >= toggleAngle && vrCamera.eulerAngles.x < 90.0f`
</br></br>
Како последен чекор го дизајнирав теренот во кој треба да се движи играчот. За оваа цел си помогнав со новоимпортирани `Assets`. На некои од нив додадов `Colliders` за да се постигне правилно движење на играчот (да може да застане на мостот и да не падне од страните - `Box Collider` & `Mesh Collider`, да не потоне под нивото на водата - `Mesh Collider`, да не оди низ камењата - `Mesh Collider`, да не се доближи до големото централно дрво - `Sphere Collider`).</br></br>
Помош при израаботка: https://www.youtube.com/watch?v=ecYezSD4qPg </br></br>
Кратка видео демонстрација како играчот се движи во околината: </br></br>
[![VRhw1 - screen recording + live demo](https://i.ytimg.com/vi/qi6A0RBGAYU/hqdefault.jpg)](https://www.youtube.com/watch?v=qi6A0RBGAYU)
