[Új szöveges dokumentum.txt](https://github.com/user-attachments/files/18688685/Uj.szoveges.dokumentum.txt)

# Jegyzőkönyv: Hálózati konfiguráció és tesztelés

## Bevezetés

Ez a jegyzőkönyv a Linksys router beállítását és a hozzá kapcsolódó hálózati eszközök tesztelését dokumentálja. A feladat során IP-címek kezelése, routing tábla megtekintése, ping tesztek és egyéb hálózati parancsok alkalmazása történt.




## Eszközök
A tesztelés során a következő eszközökkel dolgoztam:
- **Cisco Catalyst 1000 switch**: A hálózati eszközök közötti kapcsolatot biztosította.
- **Tenda router**: A hálózat központi irányítószerveként szerepelt.
- **HP Probox laptop**: A teszteléshez használt számítógép, amelyről a ping tesztek és egyéb parancsok futtak.
- **Redmi Note 12 5G**: Ezzel csatlakoztam a Linksys routerhez, hogy a laptop és a többi eszköz között pingelni tudjak.
## 1. A számítógép IP beállításainak lekérdezése
Parancs: `ipconfig`
<details>
  <summary>Kép megtekintése</summary>

![Képernyőkép 2025-02-06 113859](https://github.com/user-attachments/assets/ab082a7d-f3ae-4017-a0d0-46c5d5ad216b)

</details>

## 2. Az aktuális IP-cím eldobása
Parancs: `ipconfig /release`
<details>

  <summary>Kép megtekintése</summary>

![Képernyőkép 2025-02-06 114100](https://github.com/user-attachments/assets/78166b0e-d362-4f32-8808-6514e56f1c41)

</details>

## 3. Új IP-cím kérése
Parancs: `ipconfig /renew`
<details>

  <summary>Kép megtekintése</summary>

![Képernyőkép 2025-02-06 114457](https://github.com/user-attachments/assets/cc64cf59-2523-4a96-9d95-ec1b15703552)

</details>

## 4. A routing tábla megjelenítése
Parancs: `netstat -a`
<details>

  <summary>Config megtekintése</summary>

 [Uploading Új sC:\Users\Tanulo>netstat -a

Active Connections

  ***Proto  Local Address          Foreign Address        State
  TCP    0.0.0.0:135            Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:445            Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:5040           Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:7680           Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:11100          Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:49664          Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:49665          Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:49666          Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:49667          Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:49668          Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:49669          Fizikai-02:0           LISTENING  
  TCP    0.0.0.0:49671          Fizikai-02:0           LISTENING  
  TCP    127.0.0.1:11200        Fizikai-02:0           LISTENING  
  TCP    127.0.0.1:11300        Fizikai-02:0           LISTENING  
  TCP    127.0.0.1:11300        Fizikai-02:55592       ESTABLISHED  
  TCP    127.0.0.1:55592        Fizikai-02:11300       ESTABLISHED  
  TCP    169.254.246.178:139    Fizikai-02:0           LISTENING  
  TCP    192.168.9.193:139      Fizikai-02:0           LISTENING  
  TCP    192.168.9.196:139      Fizikai-02:0           LISTENING  
  TCP    192.168.9.196:57986    20.199.120.151:https   ESTABLISHED  
  TCP    192.168.9.196:59852    wo-in-f188:5228        ESTABLISHED  
  TCP    192.168.9.196:59853    wo-in-f188:5228        ESTABLISHED  
  TCP    192.168.9.196:60469    lb-140-82-113-25-iad:https  ESTABLISHED  
  TCP    192.168.9.196:63411    bud02s35-in-f10:https  ESTABLISHED  
  TCP    192.168.9.196:64774    bud02s39-in-f10:https  ESTABLISHED  
  TCP    192.168.9.196:64824    a23-40-158-218:http    ESTABLISHED  
  TCP    192.168.9.196:64825    40.126.31.3:https      TIME_WAIT  
  TCP    192.168.9.196:64853    LenovoSRV:epmap        TIME_WAIT  
  TCP    192.168.9.196:64854    LenovoSRV:49668        TIME_WAIT  
  TCP    192.168.9.196:64856    bud02s34-in-f14:https  TIME_WAIT  
  TCP    192.168.9.196:64863    13.89.179.14:https     TIME_WAIT  
  TCP    192.168.9.196:64864    bud02s43-in-f14:https  TIME_WAIT  
  TCP    192.168.9.196:64866    LenovoSRV:epmap        TIME_WAIT  
  TCP    192.168.9.196:64867    LenovoSRV:49668        TIME_WAIT  
  TCP    192.168.9.196:64868    13.89.179.14:https     TIME_WAIT  
  TCP    192.168.9.196:64869    bud02s34-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64870    bud02s37-in-f14:https  TIME_WAIT  
  TCP    192.168.9.196:64872    13.89.179.14:https     TIME_WAIT  
  TCP    192.168.9.196:64873    bud02s34-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64874    13.89.179.14:https     TIME_WAIT  
  TCP    192.168.9.196:64876    LenovoSRV:epmap        TIME_WAIT  
  TCP    192.168.9.196:64877    LenovoSRV:49668        TIME_WAIT  
  TCP    192.168.9.196:64878    bud02s34-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64879    bud02s37-in-f14:https  TIME_WAIT  
  TCP    192.168.9.196:64881    bud02s37-in-f3:https   TIME_WAIT  
  TCP    192.168.9.196:64883    bud02s33-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64885    13.107.21.239:https    TIME_WAIT  
  TCP    192.168.9.196:64889    a-0003:https           TIME_WAIT  
  TCP    192.168.9.196:64890    204.79.197.239:https   TIME_WAIT  
  TCP    192.168.9.196:64893    150.171.27.10:https    TIME_WAIT  
  TCP    192.168.9.196:64895    13.107.253.45:https    TIME_WAIT  
  TCP    192.168.9.196:64901    13.107.21.239:https    TIME_WAIT  
  TCP    192.168.9.196:64903    bud02s37-in-f3:https   TIME_WAIT  
  TCP    192.168.9.196:64904    bud02s33-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64906    13.107.42.14:https     TIME_WAIT  
  TCP    192.168.9.196:64911    104.17.201.65:https    TIME_WAIT  
  TCP    192.168.9.196:64912    a0f671730127a0812:https  TIME_WAIT  
  TCP    192.168.9.196:64913    172.241.51.69:https    TIME_WAIT  
  TCP    192.168.9.196:64914    952:https              TIME_WAIT  
  TCP    192.168.9.196:64915    166:https              TIME_WAIT  
  TCP    192.168.9.196:64916    213:https              TIME_WAIT  
  TCP    192.168.9.196:64917    133:https              TIME_WAIT  
  TCP    192.168.9.196:64918    172.241.51.69:https    TIME_WAIT  
  TCP    192.168.9.196:64919    133:https              TIME_WAIT  
  TCP    192.168.9.196:64920    150.171.27.10:https    TIME_WAIT  
  TCP    192.168.9.196:64921    a23-35-209-170:http    TIME_WAIT  
  TCP    192.168.9.196:64922    a23-35-209-170:http    TIME_WAIT  
  TCP    192.168.9.196:64929    a-0003:https           TIME_WAIT  
  TCP    192.168.9.196:64930    bud02s34-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64932    FujitsuSRV:microsoft-ds  ESTABLISHED  
  TCP    192.168.9.196:64934    bud02s37-in-f14:https  TIME_WAIT  
  TCP    192.168.9.196:64935    bud02s34-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64936    218:https              TIME_WAIT  
  TCP    192.168.9.196:64938    104.17.25.14:https     TIME_WAIT  
  TCP    192.168.9.196:64939    bud02s34-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64940    218:https              TIME_WAIT  
  TCP    192.168.9.196:64941    bud02s33-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64942    13.107.253.45:https    TIME_WAIT  
  TCP    192.168.9.196:64944    150.171.27.10:https    TIME_WAIT  
  TCP    192.168.9.196:64947    bud02s34-in-f10:https  TIME_WAIT  
  TCP    192.168.9.196:64948    bud02s43-in-f14:https  TIME_WAIT  
  TCP    192.168.9.196:64949    bud02s37-in-f14:https  TIME_WAIT  
  TCP    192.168.9.196:64950    bud02s37-in-f3:https   TIME_WAIT  
  TCP    [::]:135               Fizikai-02:0           LISTENING  
  TCP    [::]:445               Fizikai-02:0           LISTENING  
  TCP    [::]:2869              Fizikai-02:0           LISTENING  
  TCP    [::]:7680              Fizikai-02:0           LISTENING  
  TCP    [::]:11100             Fizikai-02:0           LISTENING  
  TCP    [::]:49664             Fizikai-02:0           LISTENING  
  TCP    [::]:49665             Fizikai-02:0           LISTENING  
  TCP    [::]:49666             Fizikai-02:0           LISTENING  
  TCP    [::]:49667             Fizikai-02:0           LISTENING  
  TCP    [::]:49668             Fizikai-02:0           LISTENING  
  TCP    [::]:49669             Fizikai-02:0           LISTENING  
  TCP    [::]:49671             Fizikai-02:0           LISTENING  
  TCP    [::1]:49670            Fizikai-02:0           LISTENING  
  UDP    0.0.0.0:123            *:*  
  UDP    0.0.0.0:5050           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5353           *:*  
  UDP    0.0.0.0:5355           *:*  
  UDP    0.0.0.0:65397          *:*  
  UDP    127.0.0.1:1900         *:*  
  UDP    127.0.0.1:49597        *:*  
  UDP    127.0.0.1:49600        *:*  
  UDP    127.0.0.1:51004        *:*  
  UDP    127.0.0.1:55002        *:*  
  UDP    169.254.246.178:137    *:*  
  UDP    169.254.246.178:138    *:*  
  UDP    169.254.246.178:1900   *:*  
  UDP    169.254.246.178:51001  *:*  
  UDP    192.168.9.193:137      *:*  
  UDP    192.168.9.193:138      *:*  
  UDP    192.168.9.193:1900     *:*  
  UDP    192.168.9.193:51003    *:*  
  UDP    192.168.9.196:137      *:*  
  UDP    192.168.9.196:138      *:*  
  UDP    192.168.9.196:1900     *:*  
  UDP    192.168.9.196:51002    *:*  
  UDP    [::]:123               *:*  
  UDP    [::]:5353              *:*  
  UDP    [::]:5353              *:*  
  UDP    [::]:5353              *:*  
  UDP    [::]:5353              *:*  
  UDP    [::]:5353              *:*  
  UDP    [::]:5353              *:*  
  UDP    [::]:5353              *:*  
  UDP    [::]:5355              *:*  
  UDP    [::1]:1900             *:*  
  UDP    [::1]:51000            *:*  
  UDP    [fe80::8707:3a9:4ffb:32b4%21]:1900  *:*  
  UDP    [fe80::8707:3a9:4ffb:32b4%21]:50997  *:*  
  UDP    [fe80::a46b:3fb2:a2e4:aab0%17]:1900  *:*  
  UDP    [fe80::a46b:3fb2:a2e4:aab0%17]:50998  *:*  
  UDP    [fe80::f0bb:57a:c8f7:b03a%10]:1900  *:*  
  UDP    [fe80::f0bb:57a:c8f7:b03a%10]:50999  *:****  
  
</details>

## 5. A microsoft.com szerver elérhetőségének tesztelése
Parancs: `ping microsoft.com`
<details>

  <summary>Kép megtekintése</summary>

![Képernyőkép 2025-02-06 115722](https://github.com/user-attachments/assets/2a687fdb-587f-42e7-b8c6-33f2198c8a39)

</details>

## 6. Az www.ipon.hu szerver felé vezető útvonal lekövetése
Parancs: `tracert www.ipon.hu`
<details>

  <summary>Kép megtekintése</summary>

![Képernyőkép 2025-02-06 120031](https://github.com/user-attachments/assets/7344a603-68c9-43d2-996e-fdf32cda632f)

</details>

## 7. Használt portok listázása
Parancs: `netstat -f`
<details>

  <summary>Config megtekintése</summary>

***C:\Users\Tanulo>netstat -f**  
 
***Active Connections**  

  ***Proto  Local Address          Foreign Address        State  
  TCP    127.0.0.1:11300        Fizikai-02.kkszki.local:55592  ESTABLISHED  
  TCP    127.0.0.1:55592        Fizikai-02.kkszki.local:11300  ESTABLISHED  
  TCP    192.168.9.196:2869     192.168.9.254:33935    TIME_WAIT  
  TCP    192.168.9.196:2869     192.168.9.254:33936    TIME_WAIT  
  TCP    192.168.9.196:2869     192.168.9.254:33938    TIME_WAIT  
  TCP    192.168.9.196:57986    20.199.120.151:https   ESTABLISHED  
  TCP    192.168.9.196:59853    wo-in-f188.1e100.net:5228  ESTABLISHED  
  TCP    192.168.9.196:64774    bud02s39-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:64824    a23-40-158-218.deploy.static.akamaitechnologies.com:http  ESTABLISHED  
  TCP    192.168.9.196:65234    bud02s43-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65237    bud02s34-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65251    bud02s34-in-f14.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65252    bud02s39-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65274    lb-140-82-113-26-iad.github.com:https  ESTABLISHED  
  TCP    192.168.9.196:65284    FujitsuSRV.kkszki.local:microsoft-ds  ESTABLISHED  
  TCP    192.168.9.196:65302    a2-18-69-178.deploy.static.akamaitechnologies.com:https  ESTABLISHED  
  TCP    192.168.9.196:65303    bud02s39-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65304    108.141.15.7:https     ESTABLISHED  
  TCP    192.168.9.196:65308    LenovoSRV.kkszki.local:epmap  TIME_WAIT  
  TCP    192.168.9.196:65309    LenovoSRV.kkszki.local:49668  TIME_WAIT  
  TCP    192.168.9.196:65312    bud02s42-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65313    bud02s42-in-f4.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65314    muc03s07-in-f99.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65315    wb-in-f84.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65316    bud02s33-in-f10.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65317    bud02s33-in-f10.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65318    bud02s41-in-f14.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65319    bud02s38-in-f10.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65320    bud02s37-in-f1.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65321    bud02s38-in-f10.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65322    bud02s39-in-f14.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65323    bud02s39-in-f14.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65324    bud02s38-in-f3.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65325    bud02s41-in-f14.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65326    wb-in-f188.1e100.net:5228  ESTABLISHED  
  TCP    192.168.9.196:65327    bud02s37-in-f1.1e100.net:https  TIME_WAIT  
  TCP    192.168.9.196:65328    bud02s38-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65329    bud02s43-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65330    bud02s39-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65332    bud02s43-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65333    bud02s37-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65334    bud02s37-in-f1.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65335    bud02s38-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65336    wb-in-f84.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65337    bud02s43-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65338    bud02s33-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65339    bud02s35-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65340    bud02s43-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65341    bud02s33-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65342    bud02s33-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65343    bud02s41-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65344    bud02s38-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65345    bud02s37-in-f1.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65346    bud02s38-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65347    bud02s37-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65348    wb-in-f84.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65349    bud02s37-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65350    bud02s33-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65351    bud02s39-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65352    bud02s39-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65353    bud02s28-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65354    bud02s43-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65355    bud02s37-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65358    bud02s39-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65359    bud02s33-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65360    bud02s38-in-f10.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65364    218.138.forpsi.net:https  ESTABLISHED  
  TCP    192.168.9.196:65365    199.232.17.91:https    ESTABLISHED  
  TCP    192.168.9.196:65366    218.138.forpsi.net:https  ESTABLISHED  
  TCP    192.168.9.196:65367    bud02s43-in-f14.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65370    bud02s38-in-f3.1e100.net:https  ESTABLISHED  
  TCP    192.168.9.196:65375    LenovoSRV.kkszki.local:epmap  TIME_WAIT  
  TCP    192.168.9.196:65376    LenovoSRV.kkszki.local:49668  TIME_WAIT  
  TCP    192.168.9.196:65377    123.35.104.34.bc.googleusercontent.com:http  ESTABLISHED  
  TCP    192.168.9.196:65379    192.168.9.254:12755    TIME_WAIT  
  TCP    192.168.9.196:65384    192.168.9.254:12755    TIME_WAIT  
  TCP    192.168.9.196:65395    192.168.9.254:12755    TIME_WAIT  
  TCP    192.168.9.196:65451    192.168.9.254:12755    TIME_WAIT  
  TCP    192.168.9.196:65455    192.168.9.254:12755    TIME_WAIT***

</details>

## 8. Hálózati kapcsolatok megjelenítése
Parancs: `netsh interface show interface`
<details>

  <summary>Kép megtekintése</summary>

![Képernyőkép 2025-02-06 120548](https://github.com/user-attachments/assets/2f889dcf-0cc8-4c52-aafd-2c37508b8c60)

</details>

## 9. DNS-beállítások aktualizálása
Parancs: `ipconfig /flushdns`
<details>

  <summary>Kép megtekintése</summary>

  ![flushdns](https://github.com/PavlyasB/IPhalo/blob/main/Képek/dnsflush.png?raw=true)

</details>

## 10. Csatolt hálózati meghajtók megjelenítése
Parancs: `net use`
<details>

  <summary>Kép megtekintése</summary>

  ![netuse](https://github.com/PavlyasB/IPhalo/blob/main/Képek/netuse.png?raw=true)

</details>

## 11. A www.ipon.hu tartománynév és IP-cím megjelenítése
Parancs: `nslookup www.ipon.hu`
<details>

  <summary>Kép megtekintése</summary>

  ![Ipon](https://github.com/PavlyasB/IPhalo/blob/main/Képek/ipon.png?raw=true)

</details>

## 12. Telefon rákapcsolódva a Wi-Fi-re
<details>
  <summary>Kép megtekintése</summary>

  ![telcsati](https://github.com/PavlyasB/IPhalo/blob/main/Képek/telefoncsati.PNG?raw=true)
</details>

## 13. Telefon pingelése laptopról
<details>
  <summary>Kép megtekintése</summary>

  ![telping](https://github.com/PavlyasB/IPhalo/blob/main/Képek/Telefon-ping.png?raw=true)
</details>

## 14. Router konfigurációk
<details>
  <summary>Kép megtekintése</summary>

  ![routercon](https://github.com/PavlyasB/IPhalo/blob/main/Képek/routerconfig.png?raw=true)
</details>

<details>
  <summary>Kép megtekintése</summary>

  ![routercon1](https://github.com/PavlyasB/IPhalo/blob/main/Képek/routerjelszo.png?raw=true)
</details>

<details>

  <summary>Kép megtekintése</summary>

  ![routercon2](https://github.com/PavlyasB/IPhalo/blob/main/Képek/pingletilt.png?raw=true)
</details>

## Összegzés
A tesztelés során a **Linksys router**, a **Catalyst 2950 switch** és a többi hálózati eszköz zökkenőmentesen működtek együtt. Az IP-konfigurációk kezelése, a routing tábla megjelenítése és a különböző hálózati parancsok futtatása sikeresen zajlott. A mobiltelefonnal való csatlakozás lehetővé tette a laptop és a többi eszköz közötti kommunikációt.
