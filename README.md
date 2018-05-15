# Project 7 - WordPress Pentesting

Time spent: **13** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) XSS
  - [ ] Summary: XSS in Comments, in version 4.2. 1st WP identified vulnerability.
    - Vulnerability types: Unauthenticated Stored XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: https://gph.is/2IgaSc3
  - [ ] Steps to recreate: Okay, so I used WP scan.  You can do a XSS, so long as the comment is over 
64kb, hence all the As in the comment you see. You leave a comment, using a XSS, that is over 64kb. If it is under that length, it doesn't allow it to work. If it is over that length, the system can't properly sanitize the comment. The comment I used was <a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAAAAAAAAAAAAAAAAAAA...(over 64kbs worth)'></a>
  - [ ] Affected source code: class="comment-reply-link" href="/?replytocom=3#respond" onclick="return addComment.moveForm( &quot;div-comment-3&quot;, &quot;3&quot;, &quot;respond&quot;, &quot;3&quot; )" aria-label="Reply to IsabellaRaymond">Reply</a>
    - [Link 1]) https://klikki.fi/adv/wordpress2.html
1. (Required) Vulnerability Name or ID
  - [ ] Summary: The Vulnerability is in the version number
    - Vulnerability types: Fingerprinting
    - Tested in version: 4.2
    - Fixed in version: In a sense, it has not been fixed because so long as they advertise their version number in any version, a hacker can conduct research on possible exploits for that version. 
  - [ ] GIF Walkthrough: https://gph.is/2L2rG48
  - [ ] Steps to recreate: Using your WP scan, it will tell you that there is a vulnerability on the page, because it tells you the version number. Navigate to the page, and you can see the version number at the top.  It is an old version number, indicating a need to update, and alerting us that patches on known exploits will not be in place. 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
