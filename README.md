# js-ipld-wasm

An ipld codec for wasm blobs allowing path traversals across Wasm modules

**WIP**

## Install

```
git clone https://github.com/korede-ta/js-ipld-wasm
npm install
```

## About

This is an IPLD codec that handles Wasm block.

Represented, in rough accordance with the [spec](http://webassembly.github.io/spec/js-api/index.html#modules)

```
{
	"module": {
		"types": [
			{
				"name": "...",
				"body": {
					"kind": ("function" | "table" | "memory" | "global"),
				}
			},
			...
		],
		"exports": [
			{
				"kind": ("function" | "table" | "memory" | "global"),
				"name": "...",
				"object": <LINK>
			},
			...
		],
		"imports": [
			{
				"module": "...",
				"kind": ("function" | "table" | "memory" | "global"),
				"name": "...",
				"object": <LINK>
			},
			...
		],
		"start": {
			"function_name": "...",
			"function": <LINK>
		},
		"globals": [
			{
				"name": "",
				"type": WASM_TYPE,
			},
			...
		],
		"memory": {
				
		},
		"data": [
			{
				segment: 
			},
			...
		],
		"table": {},
		"elements": [],
		"functions": [
			"name": "...",
			"signature": {
				"arguments": [
					{
						"name": "...",
						"type": WASM_TYPE
					},
					...
				]
				"return_type": WASM_TYPE
			},
			"code_link": <LINK>
		],
		"code": [
			{
				function: <LINK>
				function_body: <LINK>
			}
		]
		"sections": {
			"module": <LINK>,
			"name": "..."
		}
	}
}
```
