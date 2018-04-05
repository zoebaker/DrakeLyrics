```{r eval=TRUE}
install.packages('gridExtra')#viewing multiple plots together
install.packages('tidytext')
install.packages('wordcloud2')
install.packages('rvest')
install.packages('dplyr')
install.packages('xml2')
```

```{r eval=TRUE}
install.packages('gridExtra')#viewing multiple plots together
install.packages('tidytext')
install.packages('wordcloud2')
install.packages('rvest')
install.packages('dplyr')
install.packages('xml2')
```

```{r eval=TRUE}
basic_scrape <- function(input_url, tag){
  website<- read_html(input_url)
  scraped<- html_nodes(website, tag)
  scraped<- html_text(scraped)
  return (scraped)
}

viewsSongs<- basic_scrape('https://genius.com/albums/Drake/Views','.chart_row-content-title')

print(viewsSongs)
```
