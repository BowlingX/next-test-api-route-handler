[**next-test-api-route-handler**](../README.md) • **Docs**

***

[next-test-api-route-handler](../README.md) / NtarhInit

# Interface: NtarhInit\<NextResponseJsonType\>

**`Internal`**

## Extended by

- [`NtarhInitAppRouter`](NtarhInitAppRouter.md)
- [`NtarhInitPagesRouter`](NtarhInitPagesRouter.md)

## Type Parameters

• **NextResponseJsonType** = `unknown`

## Properties

### rejectOnHandlerError?

> `optional` **rejectOnHandlerError**: `boolean`

If `false`, errors thrown from within a handler are kicked up to Next.js's
resolver to deal with, which is what would happen in production. If `true`,
the [testApiHandler](../functions/testApiHandler.md) function will reject immediately instead.

You should use `rejectOnHandlerError` whenever you want to manually handle
an error that bubbles up from your handler (which is especially true if
you're using `expect` _within_ your handler) or when you notice a false
negative despite exceptions being thrown.

#### Default

```ts
false
```

#### Defined in

[index.ts:122](https://github.com/Xunnamius/next-test-api-route-handler/blob/37c35c31591639add2ada76a3899ced1163c4aeb/src/index.ts#L122)

***

### test()

> **test**: (`parameters`) => [`Promisable`](../type-aliases/Promisable.md)\<`void`\>

`test` is a function that runs your test assertions. This function receives
one destructured parameter: `fetch`, which is equivalent to
`globalThis.fetch` but with the first parameter omitted.

#### Parameters

• **parameters**

• **parameters.fetch**

#### Returns

[`Promisable`](../type-aliases/Promisable.md)\<`void`\>

#### Defined in

[index.ts:128](https://github.com/Xunnamius/next-test-api-route-handler/blob/37c35c31591639add2ada76a3899ced1163c4aeb/src/index.ts#L128)
