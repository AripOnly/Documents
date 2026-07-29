# fs/promises

## Import

``` javascript
import fs from "fs/promises";
```

------------------------------------------------------------------------

## Read File

``` javascript
const text = await fs.readFile("./data.txt", "utf8");
console.log(text);
```

------------------------------------------------------------------------

## Write File

``` javascript
await fs.writeFile("./data.txt", "Hello World", "utf8");
```

------------------------------------------------------------------------

## Append File

``` javascript
await fs.appendFile("./log.txt", "New log\n", "utf8");
```

------------------------------------------------------------------------

## Check File Exists

``` javascript
try {
  await fs.access("./config.json");
  console.log("File exists.");
} catch {
  console.log("File does not exist.");
}
```

------------------------------------------------------------------------

## Create Directory

``` javascript
await fs.mkdir("./data", {
  recursive: true,
});
```

------------------------------------------------------------------------

## Read Directory

``` javascript
const files = await fs.readdir("./src");
console.log(files);
```

------------------------------------------------------------------------

## Delete File

``` javascript
await fs.unlink("./temp.txt");
```

------------------------------------------------------------------------

## Delete Directory

``` javascript
await fs.rm("./cache", {
  recursive: true,
  force: true,
});
```

------------------------------------------------------------------------

## File Information

``` javascript
const stat = await fs.stat("./config.json");

console.log(stat.isFile());
console.log(stat.isDirectory());
console.log(stat.size);
```

------------------------------------------------------------------------

## Copy File

``` javascript
await fs.copyFile("./a.txt", "./b.txt");
```

------------------------------------------------------------------------

## Rename / Move File

``` javascript
await fs.rename("./old.txt", "./new.txt");
```

------------------------------------------------------------------------

## Read JSON

``` javascript
const text = await fs.readFile("./config.json", "utf8");
const config = JSON.parse(text);

console.log(config);
```

------------------------------------------------------------------------

## Write JSON

``` javascript
const config = {
  provider: "gemini",
  model: "gemini-3.5-flash",
};

await fs.writeFile(
  "./config.json",
  JSON.stringify(config, null, 2),
  "utf8"
);
```

------------------------------------------------------------------------

## Error Handling

``` javascript
async function loadConfig() {
  try {
    const text = await fs.readFile("./config.json", "utf8");
    return JSON.parse(text);
  } catch (error) {
    console.error("Failed to load config:", error.message);
    return null;
  }
}

const config = await loadConfig();
```
