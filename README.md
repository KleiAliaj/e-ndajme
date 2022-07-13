
<p align="center">
    <img alt="splitio" height="75" src="./static/favicon.png">
    <h1 align="center">e-ndajme</h1>
</p>

<p align="center">
  <a aria-label="Website" href="https://splitio.vercel.app" target="_blank">
    <img alt="Website" src="https://img.shields.io/website?down_color=red&down_message=offline&style=flat-square&up_message=up&url=https%3A%2F%2Fsplitio.vercel.app" />
  </a>
  <a aria-label="License" href="https://github.com/cryptoboid/splitio/blob/main/LICENSE" target="_blank">
    <img alt="License: AGPL" src="https://img.shields.io/github/license/cryptoboid/splitio?style=flat-square" target="_blank" />
  </a>
</p>

<p align="center">
ndani me lehtësi faturat tuaja! e-ndajme është një aplikacion ueb me i krijuar për të gjurmuar borxhet dhe
pagesa shpejt, pa asnjë llogari përdoruesi.
</p>
<p align="center">
informacioni shpërndahet p2p duke përdorur armë dhe enkriptohet nga skaji në skaj duke përdorur armë/det.
</p>
<p align="center">
ndertuar nga klei</p>

## 🤔 how to use



## 🌟 showcase
<table>
<tr>
    <a href=""><img width="21%" src="./screenshots/screen1.png"/></a>
    <a href=""><img width="21%" src="./screenshots/screen4.png"/></a>
    <a href=""><img width="21%" src="./screenshots/screen2.png"/></a>
    <div/>
</tr>
<tr>
    <a href=""><img width="21%" src="./screenshots/screen3.png"/></a>
    <a href=""><img width="21%" src="./screenshots/screen5.png"/></a>
    <a href=""><img width="21%" src="./screenshots/screen6.png"/></a>

</tr>
</table>

## 📝 next steps

some extra desired features/fixes are:
- better storage persistance with ["persistent" mode](https://developer.mozilla.org/en-US/docs/Web/API/Storage_API#box_modes)
- implement own relays with [write protections](https://github.com/cryptoboid/splitio/issues/19) --> [in progress!](https://github.com/cryptoboid/splitio/commit/786445f79cd4a10ea9762dbfcb2ed24737086c2d)
- ~~compute who-owes-what~~ (done!)
- ~~add settlements~~ (done! just click on who you want to pay in the balances dialog)
- ~~show date in group transactions~~ (done!)
- ~~show recently viewed groups in home~~ (done!)
- ~~favorite a group for easy access in PWA (or provide some kind of shortcut)~~ (disabled PWA for now)
- ~~support for more complex expenses: shared payment, divide by a subgroup~~ (must change storage model, too complicated for now)
- ... and more!

## ❤️ contribute

1. clone repo
2. install npm packages: `npm install`
3. start the server (with hot reloading): `npm run dev`
4. navigate to [localhost:3000](http://localhost:5000)

## ⚠️ disclaimer

even though all information is encrypted and decrypted on-device (e2ee), i'm not a security expert. given this, i'm looking for more people to review the encryption code and fix any vulnerabilities.

also, as the code uses Gun with community servers and localStorage, persisting data for long amounts of time could be an issue. try to open your group often to get more devices updated. in the future, i should probably self-host a Gun relay, though i don't currently have the means necessary.

## ⚖️ license

AGPL
