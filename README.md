### htermPath
The simplest way to add hterm to your project!

> [!IMPORTANT]  
> There aren't any type declarations in this project. Sorry.

**To install it:**
```shell
npm install hterm-path vite-plugin-static-copy express
```

**To use it with Vite (example):**
```typescript
//...
import { htermPath } from "hterm-path";
import { viteStaticCopy } from "vite-plugin-static-copy";

//...
plugins: [
    viteStaticCopy({
        //...
        targets: [
            {
                src: htermPath,
                dest: "",
                rename: "hterm"
            }
        ]
        //...
    })
]
```

**To use it with Express (example):**
```typescript
//...
import express from "express";
import { htermPath } from "hterm-path";

//...
const app = express();

//...
app.use("/hterm/", express.static(htermPath));
//...
```