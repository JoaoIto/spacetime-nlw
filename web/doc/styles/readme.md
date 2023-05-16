# IMPORTANDO A FONTE NEXTJS 

1. Importe primeiro a partir do arquivo do next no google;

```tsx
import { Roboto_Flex as Roboto, Bai_Jamjuree as BaiJam } from 'next/font/google'
```

2. Crie as variáveis ambiente e suas propriedades;
```tsx
const roboto = Roboto({ subsets: ['latin'], variable: '--font-roboto' })
const baijam = BaiJam({
  subsets: ['latin'],
  weight: '700',
  variable: '--font-baijam',
})
```

3. Depois no tailwindcss, crie as variáveis css para tal
```tsx
fontFamily: {
        sans: 'var(--font-roboto)',
        alt: 'var(--font-baijam)',
      },
```

4. Use no arquivo de layout com as variáveis tailwind e JS

```tsx
<body className={`font-sans ${roboto.variable} ${baijam.variable}`}>
        {children}
</body>
```

5. Use as variáveis no arquivo destinado

```tsx
 <h1 className="font-sans text-4xl font-bold">Sua cápsula do tempo</h1>
      <h1 className="font-alt text-4xl font-bold">Sua cápsula do tempo</h1>
   
```

---