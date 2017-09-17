#fonttools guide
1. install python in System
2. install packet - pip install fonttools
3. pyftsubset font-original.ttf --output-file=font-result.woff --unicodes-file=codes.txt
4. Convert result file into woff and woff2
5. install converter to woff - npm i -g ttf2woff
6. install converter to worff2 - npm i -g ttf2woff2
7. ttf2woff font-result.ttf font-converted.woff
8. cat font-result.ttf | ttf2woff2 >> font-converted.woff2
9. include in css
```
@font-face {
    font-family: 'myfont';
    src: url(font-converted.woff2) format('woff2'), url(font-converted.woff) format('woff');
    font-weight: normal;
    font-style: normal
    font-display: swap;
}