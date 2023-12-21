p a r s i n g d a t a
l i b r a r y ( r v e s t )
ASIN_code = " B08BG1JSCQ "
source ( " h t t p s : / /raw . gi t hu bu se r c o n te n t . com/ r j s a i t o / Ju s t−R−Things / mas ter /
t%20Mining / amazonscraper . R" )
d a t a s e t =NULL
pages = 2341
f o r ( page_num in 1 : pages ) {
u r l = p a s te 0 ( " h t tp : / /www. amazon . com/ product−reviews / " ,ASIN_code , " / ?
pageNumber= " , page_num)
doc = read _html ( u r l )
reviews = amazon_ s c r ap e r ( doc , reviewer = F , de lay = 2 )
d a t a s e t = rbind ( d a t a se t , reviews )
}
