---
theme: default
colorScheme: dark
---

# Mars Rover

Test-Driven development Kata

Victor, Manu, Tomas, Imanol, Jordi, Unai, Noel

---

# First iterations
<div grid="~ cols-2 gap-2">
<div>
<h4>Testing</h4>
````md magic-move

```ts

```

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})
```
````
</div>
<div>
<h4>Code</h4>
````md magic-move

```ts

```

```ts
class Rover {

}
```

```ts
class Rover {
  execute(commands: string): string {
    return '0:0:N'
  }
}
```
````

</div>
</div>

---

# First iterations
<div grid="~ cols-2 gap-2">
<div>
<h4>Testing</h4>
````md magic-move

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})
```

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})

it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})
```

````

</div>

<div>
<h4>Code</h4>
````md magic-move

```ts
class Rover {
  execute(commands: string): string {
    return '0:0:N'
  }
}
```

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    return '0:0:N'
  }
}
```
````
</div>
</div>

---

# First iterations

<div grid="~ cols-2 gap-2">
<div>
<h4>Testing</h4>
````md magic-move

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})

it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})
```

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})

it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})
```
````
</div>
<div>
<h4>Code</h4>
````md magic-move

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    if (commands === 'RR') return '0:0:S'
    return '0:0:N'
  }
}
```
````
</div>
</div>

---

# First iterations

<div grid="~ cols-2 gap-2">
<div>
<h4>Testing</h4>
````md magic-move

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})

it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})
```

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})

it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})
```
````
</div>
<div>
<h4>Code</h4>
````md magic-move

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    if (commands === 'RR') return '0:0:S'
    return '0:0:N'
  }
}
```

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    return '0:0:N'
  }
}
```
````
</div>
</div>

---

# First iterations

<div grid="~ cols-2 gap-2">
<div>
<h4>Testing</h4>
````md magic-move

```ts
it('should return 0:0:N when no command is given', () => {
  const rover = new Rover()
  const result = rover.execute('')
  expect(result).toBe('0:0:N')
})

it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})
```

```ts
it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})
```

```ts
it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})

it('should return 0:0:N given RRRR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RRRR')
  expect(result).toBe('0:0:N')
})
```
````

</div>
<div>
<h4>Code</h4>
````md magic-move

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    return '0:0:N'
  }
}
```

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    if (commands === 'RRRR') return '0:0:N'
    return '0:0:N'
  }
}
```
````
</div>
</div>

---

# First iterations - <span class="text-red-400">REFACTOR!!!</span>

<div grid="~ cols-2 gap-2">
<div>
<h4>Testing</h4>
````md magic-move

```ts
it('should return 0:0:E given R command line', () => {
  const rover = new Rover()
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})

it('should return 0:0:N given RRRR command line', () => {
  const rover = new Rover()
  const result = rover.execute('RRRR')
  expect(result).toBe('0:0:N')
})
```

```ts
it('should return 0:0:E given R command line', () => {
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})

it('should return 0:0:N given RRRR command line', () => {
  const result = rover.execute('RRRR')
  expect(result).toBe('0:0:N')
})
```

```ts
let rover: Rover

it('should return 0:0:E given R command line', () => {
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})

it('should return 0:0:N given RRRR command line', () => {
  const result = rover.execute('RRRR')
  expect(result).toBe('0:0:N')
})
```

```ts
let rover: Rover

beforeEach(() => {
  rover = new Rover()
})

it('should return 0:0:E given R command line', () => {
  const result = rover.execute('R')
  expect(result).toBe('0:0:E')
})

it('should return 0:0:S given RR command line', () => {
  const result = rover.execute('RR')
  expect(result).toBe('0:0:S')
})

it('should return 0:0:W given RRR command line', () => {
  const result = rover.execute('RRR')
  expect(result).toBe('0:0:W')
})

it('should return 0:0:N given RRRR command line', () => {
  const result = rover.execute('RRRR')
  expect(result).toBe('0:0:N')
})
```

```ts
let rover: Rover

beforeEach(() => {
  rover = new Rover()
})


```

```ts
let rover: Rover

beforeEach(() => {
  rover = new Rover()
})

it.each([

])
```

```ts
let rover: Rover

beforeEach(() => {
  rover = new Rover()
})

it.each([
  
])('should return %j when the command is %j',
  (expectedLandingPosition: string, commands: string) => {
    
  })
```

```ts
let rover: Rover

beforeEach(() => {
  rover = new Rover()
})

it.each([
  
])('should return %j when the command is %j',
  (expectedLandingPosition: string, commands: string) => {
    const result = rover.execute(commands)
    expect(result).toBe(expectedLandingPosition)
})
```

```ts {all|7|8-13|14|15-18|all}
let rover: Rover

beforeEach(() => {
  rover = new Rover()
})

it.each([
  ['0:0:N', ''],
  ['0:0:E', 'R'],
  ['0:0:S', 'RR'],
  ['0:0:W', 'RRR'],
  ['0:0:N', 'RRRR'],
  ['0:0:E', 'RRRRR'],
])('should return %j when the command is %j',
  (expectedLandingPosition: string, commands: string) => {
    const result = rover.execute(commands)
    expect(result).toBe(expectedLandingPosition)
})
```
````

</div>
<div>
<h4>Code</h4>
````md magic-move

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    if (commands === 'RRRR') return '0:0:N'
    return '0:0:N'
  }
}
```

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') return '0:0:E'
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    if (commands === 'RRRR') return '0:0:N'
    if (commands === 'RRRRR') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
class Rover {
  execute(commands: string): string {
    if (commands === 'R') {
      return '0:0:E'
    }
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    if (commands === 'RRRR') return '0:0:N'
    if (commands === 'RRRRR') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    if (commands === 'R') {
      return '0:0:E'
    }
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    if (commands === 'RRRR') return '0:0:N'
    if (commands === 'RRRRR') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    if (commands === 'R') {
      return `0:0:${compassRight[commands.length]}`
    }
    if (commands === 'RR') return '0:0:S'
    if (commands === 'RRR') return '0:0:W'
    if (commands === 'RRRR') return '0:0:N'
    if (commands === 'RRRRR') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    if (commands === 'R') {
      return `0:0:${compassRight[commands.length]}`
    }
    if (commands === 'RRRR') return '0:0:N'
    if (commands === 'RRRRR') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    if (commands === 'R') {
      return `0:0:${compassRight[commands.length]}`
    }
    if (commands === 'RRRR') return '0:0:N'
    if (commands === 'RRRRR') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    if (commands === 'R') {
      return `0:0:${compassRight[compassIndex]}`
    }
    if (commands === 'RRRR') return '0:0:N'
    if (commands === 'RRRRR') return '0:0:E'
    return '0:0:N'
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    if (commands === 'R') {
      return `0:0:${compassRight[compassIndex]}`
    }
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    return `0:0:${compassRight[compassIndex]}`
  }
}
```
````

</div>
</div>

---
src: ./pages/left.md
hide: false
---

---
layout: center
class: text-center
---

# GRACIAS!! 🚀

<div class="text-2xl">
Muchas gracias tanto a los <span class="text-purple-300">organizadores</span> como a los <span class="text-purple-300">participantes</span> de la Kata.
</div>

Si tenéis alguna <span class="text-blue-300">duda</span> no dudéis en preguntar.

Agracedemos cualquier <span class="text-blue-300">feedback</span> que nos podáis dar para mejorar.

Si quereis ver el código completo, lo teneis en <a href="https://github.com/noel-lopez/mars-rover-kata" target="_blank">este enlace</a>.