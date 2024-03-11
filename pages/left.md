
# First iterations - <span class="text-red-400">REFACTOR!!!</span>

<div grid="~ cols-2 gap-2">
<div>
<h4>Testing</h4>
````md magic-move

```ts
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
  ['0:0:W', 'L'],
  ['0:0:S', 'LL'],
  ['0:0:E', 'LLL'],
  ['0:0:N', 'LLLL'],
  ['0:0:W', 'LLLLL']
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
const compassRight = ['N', 'E', 'S', 'W']

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    return `0:0:${compassRight[compassIndex]}`
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']
const compassLeft = ['N','W','S','E'];

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    return `0:0:${compassRight[compassIndex]}`
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']
const compassLeft = ['N','W','S','E'];

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    if(commands.includes('L')){  
      
    }
    return `0:0:${compassRight[compassIndex]}`
  }
}
```

```ts
const compassRight = ['N', 'E', 'S', 'W']
const compassLeft = ['N','W','S','E'];

class Rover {
  execute(commands: string): string {
    const compassIndex = commands.length % 4
    if(commands.includes('L')){  
      return `0:0:${compassLeft[compassIndex]}`
    }
    return `0:0:${compassRight[compassIndex]}`
  }
}
```
````

</div>
</div>