 
# atom-shells-js

Einfaches Atommodell in JavaScript.

Lernprojekt, um Architekturunterschiede zu Java zu lernen.

## **Features**

- Energie für wasserstoffähnliche Systeme
- Elektronenverteilung auf Schalen
- Grafische Darstellung auf HTML-Canvas

## **How 2 Use**

Benötigt werden Node.js und das HTTP-Server-Modul.

```bash
npm install -g http-server
```

```bash
npx http-server
```

## **Architektur**

**Ordnerstruktur**

```yaml
/
│ 
├── physics/             //Physik
│     ├── atom.js
│     ├── energy.js
│     └── shells.js
│ 
├── renderer/           //Renderer
│     └── renderer.js
│ 
└── main.js             //Hauptprogramm
```

**Klassendiagramm**

```yaml
Main
│
├── Atom (Object)
│     ├── atomicNumber
│     ├── shells[]
│     ├── configuration[]
│     └── totalEnergy
│
├── Shell (Object)
│     ├── n
│     ├── electrons
│     ├── maxElectrons
│     └── energy
│
├── atom.js
│     ├── createAtom()
│     ├── calculateConfiguration()
│     └── createShells()
│
├── energy.js
│     ├── calculateEnergy()
│     └── calculateTotalEnergy()
│
└── renderer.js
      ├── drawAtom()
      ├── drawShells()
      └── drawNucleus()
```

## Siehe auch

- [atom-shells-java](https://github.com/kuranez/atom-shells-java) - Einfaches Schalenmodell (Java)
- [atom-orbitals-java (Orbitalmodell)](https://github.com/kuranez/atom-orbitals-java) - Einfaches Orbitalmodell (Java)
