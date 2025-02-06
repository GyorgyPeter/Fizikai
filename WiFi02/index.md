# Jegyzőkönyv: Hálózati konfiguráció és tesztelés

## Bevezetés

Ez a jegyzőkönyv a Linksys router beállítását és a hozzá kapcsolódó hálózati eszközök tesztelését dokumentálja. A feladat során IP-címek kezelése, routing tábla megtekintése, ping tesztek és egyéb hálózati parancsok alkalmazása történt.




## Eszközök
A tesztelés során a következő eszközökkel dolgoztam:
- **Catalyst 2950 switch**: A hálózati eszközök közötti kapcsolatot biztosította.
- **Linksys router**: A hálózat központi irányítószerveként szerepelt.
- **ThinkPad laptop**: A teszteléshez használt számítógép, amelyről a ping tesztek és egyéb parancsok futtak.
- **Mobiltelefon**: Ezzel csatlakoztam a Linksys routerhez, hogy a laptop és a többi eszköz között pingelni tudjak.
## 1. A számítógép IP beállításainak lekérdezése
Parancs: `ipconfig`
<details>
  <summary>Kép megtekintése</summary>

  ![IPCONFIG](https://github.com/PavlyasB/IPhalo/blob/main/Képek/ipconfig-all.png?raw=true)

</details>

## 2. Az aktuális IP-cím eldobása
Parancs: `ipconfig /release`
<details>

  <summary>Kép megtekintése</summary>

  ![release](https://github.com/PavlyasB/IPhalo/blob/main/Képek/iprelease.png?raw=true)

</details>

## 3. Új IP-cím kérése
Parancs: `ipconfig /renew`
<details>

  <summary>Kép megtekintése</summary>

  ![renew](https://github.com/PavlyasB/IPhalo/blob/main/Képek/iprenew.png?raw=true)

</details>

## 4. A routing tábla megjelenítése
Parancs: `netstat -a`
<details>

  <summary>Kép megtekintése</summary>

  ![netstat-a](https://github.com/PavlyasB/IPhalo/blob/main/Képek/netstat-a.png?raw=true)

</details>

## 5. A microsoft.com szerver elérhetőségének tesztelése
Parancs: `ping microsoft.com`
<details>

  <summary>Kép megtekintése</summary>

  ![microsoft](https://github.com/PavlyasB/IPhalo/blob/main/Képek/microsoftcom.png?raw=true)

</details>

## 6. Az www.ipon.hu szerver felé vezető útvonal lekövetése
Parancs: `tracert www.ipon.hu`
<details>

  <summary>Kép megtekintése</summary>

  ![tracert](https://github.com/PavlyasB/IPhalo/blob/main/Képek/traceipon.png?raw=true)

</details>

## 7. Használt portok listázása
Parancs: `netstat -f`
<details>

  <summary>Kép megtekintése</summary>

  ![netstat-f](https://github.com/PavlyasB/IPhalo/blob/main/Képek/netstat-f.png?raw=true)

</details>

## 8. Hálózati kapcsolatok megjelenítése
Parancs: `netsh interface show interface`
<details>

  <summary>Kép megtekintése</summary>

  ![netsh](https://raw.githubusercontent.com/PavlyasB/IPhalo/refs/heads/main/K%C3%A9pek/netstat-a.png)

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
