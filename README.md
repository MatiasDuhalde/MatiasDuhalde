TypeScript mfs one second after they discover the existence of `infer` :

```typescript
type CoolType<T> = T extends infer A
  ? A extends infer B
    ? B extends infer C
      ? C extends infer D
        ? D extends infer E
          ? E extends infer F
            ? F extends infer G
              ? G extends infer H
                ? H extends infer I
                  ? I extends infer J
                    ? J extends infer K
                      ? K extends infer L
                        ? L extends infer M
                          ? M extends infer N
                            ? N extends infer O
                              ? O extends infer P
                                ? P extends infer Q
                                  ? Q extends infer R
                                    ? R extends infer S
                                      ? S extends infer T
                                        ? T extends infer U
                                          ? U extends infer V
                                            ? V extends infer W
                                              ? W extends infer X
                                                ? X extends infer Y
                                                  ? Y extends infer Z
                                                    ? {
                                                        [K in keyof Z]: Z[K] extends number
                                                          ? Z[K] extends 0
                                                            ? 'zero'
                                                            : Z[K] extends 1
                                                            ? 'one'
                                                            : Z[K] extends 2
                                                            ? 'two'
                                                            : Z[K] extends 3
                                                            ? 'three'
                                                            : 'other'
                                                          : Z[K] extends string
                                                          ? Z[K] extends 'hello'
                                                            ? 'world'
                                                            : Z[K] extends 'open'
                                                            ? 'close'
                                                            : Z[K] extends 'up'
                                                            ? 'down'
                                                            : 'other'
                                                          : 'other';
                                                      }
                                                    : never
                                                  : never
                                                : never
                                              : never
                                            : never
                                          : never
                                        : never
                                      : never
                                    : never
                                  : never
                                : never
                              : never
                            : never
                          : never
                        : never
                      : never
                    : never
                  : never
                : never
              : never
            : never
          : never
        : never
      : never
    : never
  : never;

```
