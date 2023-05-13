import requests
from bs4 import BeautifulSoup

from pymongo import MongoClient
client = MongoClient('mongodb+srv://fujipan50:test1234@cluster0.x8ak7eq.mongodb.net/?retryWrites=true&w=majority')
db = client.dbsparta

# URLを読み込みHTMLを受け取る
headers = {'User-Agent' : 'Mozilla/5.0 (Windows NT 10.0; Win64; x64)AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.86 Safari/537.36'}
data = requests.get('https://www.billboard-japan.com/charts/detail?a=hot100',headers=headers)


# HTMLをBeautifulSoupというライブラリを利用し検索しやすい状態にする

soup = BeautifulSoup(data.text, 'html.parser')

# selectを利用し, ランキング全体を呼び出す
musics = soup.select('#content2 > div > div.leftBox > table > tbody > tr')

# musicsを繰り返し文で反復させる
for music in musics:
    rank = music.select_one('td > span')
    if rank is not None:
        rank = rank.text
        title = music.select_one('p.musuc_title').text.strip()
        artist = music.select_one('p.artist_name').text.strip()
    doc = {
            'rank': rank,
            'title': title,
            'artist': artist
    }
    db.musics.insert_one(doc)
    print(rank, title, artist)
