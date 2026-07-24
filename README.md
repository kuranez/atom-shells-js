 
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
│     ├── electronCount
│     ├── shells[]
│     ├── configuration[]
│     └── totalEnergy
│
├── Shell (Object)
│     ├── n
│     ├── maxElectrons
│     ├── electrons
│     └── energy
│
├── atom.js
│     ├── createAtom(atomicNumber)
│     ├── calculateConfiguration(atom)
│     └── createShells(atom)
│
├── shells.js
│     ├── createShell(n)
│     └── fillShells(atom)
│
├── energy.js
│     ├── calculateEnergy(shell)
│     └── calculateTotalEnergy(atom)
│
└── renderer.js
      ├── drawAtom(atom)
      ├── drawShells(shells)
      └── drawNucleus(atom)
```

## Siehe auch

- [atom-shells-java](https://github.com/kuranez/atom-shells-java) - Einfaches Schalenmodell (Java)
- [atom-orbitals-java (Orbitalmodell)](https://github.com/kuranez/atom-orbitals-java) - Einfaches Orbitalmodell (Java)
