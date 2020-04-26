## Welcome to GitHub Pages

# New-pandas-users-summary
This is a summary of basic functions and concepts from pandas tutorial for new users, focusing on creating dataFrame, grouping, IO, lambda, selecting data and handling indexs etc the very necessity of using pandas. 

I first list the functions together to give a overview :
## List of functions:

list
zip
*list(zip(names, numbers))*
pd.DataFrame(data = , columns=[])
df.to_csv
pd.read_csv
df.types (check datatype of column)
df.sort_values([column_name], ascending = True or False )
df.sort_index(axis=0)

random.seed()
random.randint(low = , high = )

*random_names = [names[random.randint(low=0 high = len(names))] for i in range(1000)]*

len
range
df.info()
df.describe()
df[column_name].unique()

df.groupby('index')
df.groupby().sum()

def function():
   return

pd.read_excel(path, index_col = )
df.index

*df['State'] = df.State.apply(lambda x: x.upper())*
*df = df[df['Status'] == 1]* boolean indexing

df.reset_index()
*Daily = df.reset_index().groupby(['State','StatusDate']).sum()*

del df[column_name]
df.index.levels[0]

*StateYearMonth = Daily.groupby([Daily.index.get_level_values(0), Daily.index.get_level_values(1).year, Daily.index.get_level_values(1).month])*
*Daily['Lower'] = StateYearMonth['CustomerCount'].transform(lambda x: x.quantile(q=.25) - (1.5*x.quantile(q=.75) - x.quantile(q=.25)))*
*YearMonth = All.groupby([lambda x: x.year, lambda x:x.month])*

idx = pd.date_range(start = , end = , freq= )
df = pd.DataFrame(data, index = idx, columns = [columns_name])
pd.concat()
*Year = combined.gropupby(lambda x:x.year).max()*
df.pct_change(periods = )

df.iloc[0:3]
df[column_name]
df.loc[df.index[0:3], column_name]

*d = {'one':[1,1], 'two':[2,2]}*
*i = ['a', 'b']*
*df = pd.DataFrame(data = d, index = i)*

one	two
a	1	2
b	1	2

df.stack()
a  one    1
   two    2
b  one    1
   two    2

df.unstack()
one  a    1
     b    1
two  a    2
     b    2

df.T
	a	b
one	1	1
two	2	2


end


# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/li116tao/a/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
