# Random GUID Generator
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->
Random GUID or API Generator

### Interactive Repl.it

[![Run on Repl.it](https://repl.it/badge/github/AmieDD/RandomGUIDGenerator)](https://repl.it/github/AmieDD/RandomGUIDGenerator)

```javascript
/* Create random GUID generator for API 
 Unique Identifiers
 */
function generateUUID()
{
	var d = new Date().getTime();
	
	if( window.performance && typeof window.performance.now === "function" )
	{
		d += performance.now();
	}
	
	var uuid = 'xxxxxxxx-xxxx-8xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c)
	{

		var r = (d + Math.random()*16)%16 | 0;
		d = Math.floor(d/16);
		return (c=='x' ? r : (r&0x3|0x8)).toString(16);
	});

return uuid;
}

// Generate new guid and insert into input value
 
$( '#keygen' ).on('click',function()
{
	$( '#apikey' ).val( generateUUID() );
});
```

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://www.amiedd.com"><img src="https://avatars3.githubusercontent.com/u/7669428?v=4" width="100px;" alt=""/><br /><sub><b>Amie DD</b></sub></a><br /><a href="https://github.com/AmieDD/RandomGUIDGenerator/commits?author=AmieDD" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!