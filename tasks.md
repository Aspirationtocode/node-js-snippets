# Tasks
### Show directory files tree in this format with right indentation:

file-example: `some.txt`

folder-example: `|folder|`

`Folders must go first on their lvl.`

### example:
```javascript
root
  |sub-folder1|
    |sub-folder2|
      |sub-folder3|
      filename2.ext
  filename1.ext    
```
```javascript
// const fs = require('fs');
//
// const options = {encoding: 'utf-8'};
//
// String.prototype.indexOfEnd = function(symbol) {
//   return this.split('').reverse().join('').indexOf(symbol);
// }
//
// function showOnlyName(fullDirName) {
//   const checkPoint = fullDirName.indexOfEnd('/');
//   return fullDirName.slice(-checkPoint, fullDirName.length);
// }
//
// function countSlashes(fullDirName) {
//   let count = 0;
//   for (let i = 0; i < fullDirName.length; i++) {
//     if (fullDirName[i] === '/') {
//       count++;
//     }
//   }
//   return count;
// }
//
// function showDirectoryTree(dirNameOuter) {
//   let tree = ``
//   function _showDirectoryTree(dirName) {
//     fs.readdir(dirName, options, (err, files) => {
//       files.forEach((file, i, files) => {
//         let currentPath = `${dirName}/${file}` ;
//         fs.stat(currentPath, (err, state) => {
//           let onlyName = showOnlyName(currentPath);
//           let tab = '--'.repeat(countSlashes(currentPath) - countSlashes(dirNameOuter) - 1);
//           if (state.isDirectory()) {
//             tree += `${tab}|${onlyName}|\n`;
//             _showDirectoryTree(currentPath);
//           } else {
//             tree += `${tab}${onlyName}\n`;
//           }
//         })
//       })
//     })
//   }
//
//   _showDirectoryTree(dirNameOuter);
//   setTimeout(() => {
//     console.log(tree)
//   }, 1000)
//
//
// }
//
// showDirectoryTree('./text-files');

```
