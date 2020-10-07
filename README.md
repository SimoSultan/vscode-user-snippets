# vscode-user-snippets

## SimoSultans VSCode User Snippets

![GitHub followers](https://img.shields.io/github/followers/SimoSultan?style=social)  
![Twitter Follow](https://img.shields.io/twitter/follow/simo_sultan?style=social)  
[www.simonmcurran.com](https://www.simonmcurran.com/)  


### Description

Just wanted a place to share all my (HTML & JavaScript) snippets with people who wanted them. Also, then they can get the updates when as well when I publish them.
I'm not going to talk about here how to set up the file. Go to [Lachy's Tutorial](https://github.com/LachlynR/Custom-VSCode-Snippets-Guide) on how to do this. What you do need to do though is copy over everything between the first and last curly bracket and add it in if you already have snippets in there, but if you don't, then just copy everything and paste it in. Feel free to edit them to your liking, cause they are yours now! Enjoy!
If you have questions feel free to reach out. 


### HTML Snippets

```json
{
	"jquery": {
			"prefix": "jquery",
			"body": [
				"",
				"<!-- jQuery CDN --->",
				"<script defer src='https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js%27%3E'></script>",
				"",
			],
			"description": "jQuery CDN Link"
	},

	"axios" : {
			"prefix": "axios",
			"body": [
				"",
				"<!-- Axios CDN --->",
				"<script defer src='https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js'></script>",
				"",
			],
			"description": "Axios CDN Link"
	},

	"bootstrap" : {
		"prefix": "bootstrap",
		"body": [
				"",
				"<!-- Bootstrap CDN --->",
				"<link rel='stylesheet' href='https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css' integrity='sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z' crossorigin='anonymous'>",
				"<script defer src='https://code.jquery.com/jquery-3.5.1.slim.min.js' integrity='sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj' crossorigin='anonymous'></script>",
				"<script defer src='https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js' integrity='sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN' crossorigin='anonymous'></script>",
				"<script defer src='https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js' integrity='sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV' crossorigin='anonymous'></script>",
				"<meta name='viewport' content='width=device-width, initial-scale=1, shrink-to-fit=no'>",
				"",
		],
		"description": "Boostrap CDN Link"
	},

	// "fontawesome" : {
	// 	"prefix": "fontawesome",
	// 	"body": [
	// 		"",
	// 		"<!-- FontAwesome CDN --->",
	// 	]
	// }
}
```

### JavaScript Snippets

```json
{
	"ajax": {
			"prefix": "ajax",
			"body": [
					"$.ajax({",
					"\turl: '${1:url}',",
					"\tmethod: '${2:GET}',",
					"\tdatatype: '${3:json}',",
					"\tsuccess: (data) => {",
					"\t\t${4};",
					"\t},",
					"\terror: (err) => {",
					"\t\t${5};",
					"\t}",
					"});"
			],
			"description": "Ajax user snippet"
	},

	"fetch": {
			"prefix": "fetch",
			"body": [
					"fetch(${1:url})",
					"\t.then(resp => resp.json())",
					"\t.then(data => console.log(data)",
					"\t.catch(err => console.log(err))",
			],
			"description": "fetch user snippet"
	},

	"axios": {
			"prefix": "axios",
			"body": [
					"axios",
						"\t.get(`${1:url}`, {",
							"\t\tparams: {}",
						"\t})",
						"\t.then(resp => console.log(resp));",
			],
			"description": "axios user snippet"
	},

	"capitalize" : {
		"prefix": "capitalize",
		"body": [
			"String.prototype.capitalize = function() {",
			"\treturn this.charAt(0).toUpperCase() + this.slice(1)",
			"}",
		],
		"description": "capitalize prototype function",
	},

	"sample" : {
		"prefix": "sample",
		"body": [
			"Array.prototype.sample = function() {",
			"\treturn this[Math.floor(Math.random() * this.length)]",
			"}",
		],
		"description": "get random element from array",
	},

	"sampleObjectKey" : {
		"prefix": "sampleKey",
		"body": [
			"Object.prototype.sampleKey = function() {",
			"\tconst keys = Object.keys(this)",
			"\treturn keys[Math.floor(Math.random() * keys.length)]",
			"}",
		],
		"description": "get random key from object",
	},

	"sampleObjectVal" : {
		"prefix": "sampleVal",
		"body": [
			"Object.prototype.sampleVal = function() {",
			"\tconst keys = Object.keys(this)",
			"\treturn this[keys[ keys.length * Math.random() << 0]]",
			"}",
		],
		"description": "get random value from object",
	},

	"nodeServer" : {
		"prefix": "nodeServer",
		"body": [
			"const http = require('http')",
			"const hostname= '127.0.0.1'",
			"const port= ${1:3000}",
			"",
			"const server = http.createServer((req, res) =>{",
				"\tres.statusCode = 200 //All ok, positive response",
				"\tres.setHeader('Content-Type', 'text/plain')",
				"\tres.end('Hello World')",
			"})",
			"",
			"server.listen(port, hostname, () => {",
				"\tconsole.log('server running on' + hostname + ': ' + port)",
			"})",
			"",
		],
		"description": "node server",
	},

	"express" : {
		"prefix": "express",
		"body": [
			"const express = require('express')",
			"const app = express()",
			"const port = process.env.PORT || ${1:3000}",
			"",
			"app.use( express.urlencoded( {extended: false }) )",
			"app.use( express.json() )",
			"",
			"// use means its a middle ware",
			"app.use( (req, res, next) => {",
			"\tconsole.log('Middle-ware running.')",
			"\tnext()",
			"})",
			"",
			"app.get('/', (req, res) => {",
				"\tres.send('Hello World!')",
			"})",
			"",
			"app.listen(port, () => {",
				"\tconsole.log('listening on port:' + port)",
			"})",
			"",
		],
		"description": "express plain",
	},

	"expressHandlebars" : {
		"prefix": "expressHandlebars",
		"body": [
			"const express = require('express')",
			"const exphbs  = require('express-handlebars')",
			"const app = express()",
			"const port = process.env.PORT || ${1:3000}",
			"",
			"app.engine('handlebars', exphbs())",
			"app.set('view engine', 'handlebars')",
			"",
			"app.use( express.urlencoded( {extended: false }) )",
			"app.use( express.json() )",
			"",
			"// use means its a middle ware",
			"app.use((req, res, next) => {",
			"\tconsole.log('Middle-ware running.')",
			"\tnext()",
			"})",
			"",
			"app.get('/', (req, res) => {",
				"\tres.send('Hello World!')",
			"})",
			"",
			"app.listen(port, () => {",
				"\tconsole.log('listening on port:' + port)",
			"})",
			"",
		],
		"description": "express w handlebars",
	},

	"expressRoutes": {
		"prefix": "expressRoutes",
		"body":[
			"const express = require('express')",
			"const router = express.Router()",
			"const {",
				"\tget${1:}s,",
				"\tget${1:},",
				"\tmake${1:},",
				"\tremove${1:},",
				"\tchange${1:}",
			"} = require('../controllers/${1:}s_controller')",
			"",
			"// Returns all ${1:}s",
			"router.get('/', get${1:}s)",
			"",
			"// Returns one ${1:} with given id",
			"router.get('/:id', get${1:})",
			"",
			"// Creates a new ${1:}",
			"router.${1:}('/', make${1:})",
			"",
			"// Deletes a ${1:} with given id",
			"router.delete('/:id', remove${1:})",
			"",
			"// Updates a ${1:} with given id",
			"router.patch('/:id', change${1:})",
			"",
			"module.exports = router"
		]
	},

	"expressMongoose": {
		"prefix": "expressMongoose",
		"body":[
			"const express = require('express')",
			"const app = express()",
			"const mongoose = require('mongoose')",
			"const router = require('./routes/routes')",
			"",
			"const port = process.env.PORT || ${1:3000}",
			"",
			"app.use( express.urlencoded( {extended: false }) )",
			"app.use( express.json() )",
			"",
			"// use means its a middle ware",
			"app.use((req, res, next) => {",
				"\tconsole.log('Middle-ware running.')",
				"\tnext()",
			"})",
			"",
			"app.get('/', (req, res) => {",
				"\tres.send('Hello World!')",
			"})",
			"",
			"app.use('/${2:}', router)",
			"",
			"const dbConnection = 'mongodb://localhost/${2:}'",
			"// Set three properties to avoid deprecation warnings:",
			"mongoose.connect(dbConnection, {",
							"\t\t\t\tuseNewUrlParser: true,",
							"\t\t\t\tuseUnifiedTopology: true,",
							"\t\t\t\tuseFindAndModify: false",
						"\t\t\t}, (err) => {",
							"\t\t\t\tif (err)",
								"\t\t\t\t\tconsole.log('Error connecting to database', err)",
							"\t\t\t\telse",
								"\t\t\t\t\tconsole.log('Connected to database!')",
								"\t\t\t\t\t// listen here because its successful",
								"\t\t\t\t\tconst server = app.listen(port, () => {",
									"\t\t\t\t\t\tconsole.log('listening on port:' + port)",
								"\t\t\t\t})",
			"})",
			""
		]
	},

	"expressSchema":{
		"prefix": "expressSchema",
		"body": [
			"const mongoose = require('mongoose')",
			"const Schema = mongoose.Schema",
			"",
			"// Define ${1:} schema",
			"const ${1:} = new Schema({",
				"\t${2:name}: {",
						"\t\ttype: String,",
						"\t\trequired: true,",
				"\t},",
				"\t${3:create_date}: {",
						"\t\ttype: Date,",
						"\t\trequired: true",
				"\t},",
				"\t${4:modified_date}: {",
						"\t\ttype: Date,",
						"\t\trequired: true",
				"\t}",
			"})",
			"",
			"module.exports = mongoose.model('${1:}', ${1:})"
		]
	}
}

```