# DoubanWeeklyPopularBooks
豆瓣读书一周热门图书榜的爬虫

This Jupyter Notebook contains a Python script that scrapes the top 10 books from various categories on Douban's weekly book charts. (这个Jupyter Notebook包含一个Python脚本，用于爬取豆瓣每周图书排行榜中各类别的前10本书籍。)

## Features 功能特点 
- Scrapes top 10 books from 12 different categories on Douban 从豆瓣的12个不同类别中爬取前10名的书籍
- Extracts detailed information for each book including title, author, publisher, rating, number of ratings, URL, ISBN, and description 提取每本书的详细信息，包括标题、作者、出版社、评分、评分人数、URL、ISBN和描述
- Saves the scraped data to a CSV file 将爬取的数据保存为CSV文件

## Requirements 运行要求

- Python 3.x
- Required libraries: requests, BeautifulSoup4, csv, datetime, time, os

## How it works 工作原理

1. The script defines a list of categories and their corresponding URLs on Douban. 脚本定义了豆瓣上各类别及其对应的URL列表。
2. It then iterates through each category, scraping the top 10 books' information. 然后遍历每个类别，爬取前10本书的信息。
3. For each book, it extracts basic information from the category page. 对于每本书，从类别页面提取基本信息
4. It then visits each book's individual page to fetch the ISBN and description. 然后访问每本书的单独页面以获取ISBN和描述。
5. All scraped data is collected in a list of dictionaries. 所有爬取的数据都收集在一个字典列表中。
6. Finally, the data is written to a CSV file named `top_10_books_all_categories_YYYYMMDD.csv` in a specified folder. 最后，数据被写入一个名为`top_10_books_all_categories_YYYYMMDD.csv`的CSV文件，保存在指定文件夹中。

## Usage 使用方法

1. Ensure all required libraries are installed. 确保安装了所有必需的库。
2. Run the notebook cell. 运行notebook单元格。
3. The script will execute and save the CSV file in the specified folder. 脚本将执行并在指定文件夹中保存CSV文件。

## Output

The script will create a CSV file with the following columns: 脚本将创建一个包含以下列的CSV文件：
- category
- number (ranking within category)
- title
- author
- publisher
- rating
- num_ratings
- url
- isbn
- description

## Note

- The script includes a 10-second delay between requests to avoid detection as a bot. 脚本在请求之间包含10秒的延迟，以避免被检测为机器人。
- Make sure to update the `folder_path` variable to your desired output location. 请确保更新`folder_path`变量为您想要的输出位置。
- The script uses headers to mimic a browser request. You may need to update these periodically. 脚本使用headers模仿浏览器请求。您可能需要定期更新这些信息。

## Disclaimer

This script is for educational purposes only. Be sure to comply with Douban's terms of service and robots.txt file when using this script. 此脚本仅用于教育目的。使用此脚本时，请确保遵守豆瓣的服务条款和robots.txt文件。
