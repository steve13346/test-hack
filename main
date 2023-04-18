#⠀⠀⠀⠀⠀⢸⠓⢄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
#⠀⠀⠀⠀⠀⢸⠀⠀⠑⢤⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
#⠀⠀⠀⠀⠀⢸⡆⠀⠀⠀⠙⢤⡷⣤⣦⣀⠤⠖⠚⡿⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀
#⣠⡿⠢⢄⡀⠀⡇⠀⠀⠀⠀⠀⠉⠀⠀⠀⠀⠀⠸⠷⣶⠂⠀⠀⠀⣀⣀⠀⠀⠀
#⢸⣃⠀⠀⠉⠳⣷⠞⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠉⠉⠉⠉⠉⠉⠉⢉⡭⠋
#⠀⠘⣆⠀⠀⠀⠁⠀⢀⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡴⠋⠀⠀
#⠀⠀⠘⣦⠆⠀⠀⢀⡎⢹⡀⠀⠀⠀⠀⠀⠀⠀⠀⡀⠀⠀⡀⣠⠔⠋⠀⠀⠀⠀
#⠀⠀⠀⡏⠀⠀⣆⠘⣄⠸⢧⠀⠀⠀⠀⢀⣠⠖⢻⠀⠀⠀⣿⢥⣄⣀⣀⣀⠀⠀
#⠀⠀⢸⠁⠀⠀⡏⢣⣌⠙⠚⠀⠀⠠⣖⡛⠀⣠⠏⠀⠀⠀⠇⠀⠀⠀⠀⢙⣣⠄
#⠀⠀⢸⡀⠀⠀⠳⡞⠈⢻⠶⠤⣄⣀⣈⣉⣉⣡⡔⠀⠀⢀⠀⠀⣀⡤⠖⠚⠀⠀
#⠀⠀⡼⣇⠀⠀⠀⠙⠦⣞⡀⠀⢀⡏⠀⢸⣣⠞⠀⠀⠀⡼⠚⠋⠁⠀⠀⠀⠀⠀
#⠀⢰⡇⠙⠀⠀⠀⠀⠀⠀⠉⠙⠚⠒⠚⠉⠀⠀⠀⠀⡼⠁⠀⠀⠀⠀⠀⠀⠀⠀
#⠀⠀⢧⡀⠀⢠⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠙⣞⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀
#⠀⠀⠀⠙⣶⣶⣿⠢⣄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
#⠀⠀⠀⠀⠀⠉⠀⠀⠀⠙⢿⣳⠞⠳⡄⠀⠀⠀⢀⡞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
#⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠉⠀⠀⠹⣄⣀⡤⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀


# DO NOT MODIFY ANYTHING BELOW IF YOU DO NOT KNOW WHAT YOU ARE DOING!!!

# MADE WITH LOVE BY NOAHREPUBLIC, J3LDO, SLOURN <3, POMPOMPURIN, AND DUCKYY
import requests as r
from threading import Thread
import os
import uuid
import time
import datetime
import json
import colorama

os.system("color 02")
os.system("title made with love by noahrepublic, J3LDO, slourn, and pompompurin")

with open("limiteds.txt", encoding='utf-8') as f:
    limiteds = f.read().replace(" ", "").split(",")

with open("config.json", "r", encoding="utf-8") as f:
    config = json.load(f)
    discordWebhook = config['discordWebhook']


try:
    import winreg

    path = winreg.HKEY_CURRENT_USER
    robloxcom = winreg.OpenKeyEx(path, r"SOFTWARE\\Roblox\\RobloxStudioBrowser\\roblox.com")



    cookie = str(winreg.QueryValueEx(robloxcom, ".ROBLOSECURITY")[0]) 
except:
    print(">> [LOGS] FAILED TO AUTODETECT A COOKIE")
    cookie = None


if cookie:
    cookie = cookie.split("<")[3]
    cookie = cookie.split(">")[0]
    cookie = cookie.strip()

    try:
        user_id = r.get("https://users.roblox.com/v1/users/authenticated", cookies={".ROBLOSECURITY": cookie}).json()["id"]
        print(">> [LOGS] SUCCESSFULLY AUTOMATICALLY FOUND COOKIE")
    except:
        cookie = config['cookie']
else:
    cookie = config['cookie']

with open("limiteds.txt", "r") as f:
    limiteds = f.read().replace(" ", "").split(",")

user_id = r.get("https://users.roblox.com/v1/users/authenticated", cookies={".ROBLOSECURITY": cookie}).json()["id"]
x_token = ""
def get_x_token():
    global x_token

    x_token = r.post("https://auth.roblox.com/v2/logout",
                     cookies={".ROBLOSECURITY": cookie}).headers["x-csrf-token"]
    print(">> [LOGS] LOGGED IN SUCCESSFULLY")

    while 1:
        # Gets the x_token every 4 minutes.
        x_token = r.post("https://auth.roblox.com/v2/logout",
                         cookies={".ROBLOSECURITY": cookie}).headers["x-csrf-token"]
        time.sleep(248)


def buy(json, itemid, productid):
    print(">> [LOGS] SPAM BUYING LIMITED")

    data = {
        "collectibleItemId": itemid,
        "expectedCurrency": 1,
        "expectedPrice": 0,
        "expectedPurchaserId": user_id,
        "expectedPurchaserType": "User",
        "expectedSellerId": json["creatorTargetId"],
        "expectedSellerType": "User",
        "idempotencyKey": "random uuid4 string that will be your key or smthn",
        "collectibleProductId": productid
    }

    while 1:
        data["idempotencyKey"] = str(uuid.uuid4())
        bought = r.post(f"https://apis.roblox.com/marketplace-sales/v1/item/{itemid}/purchase-item", json=data,
            headers={"x-csrf-token": x_token}, cookies={".ROBLOSECURITY": cookie})

        if bought.reason == "Too Many Requests":
            print(">> [LOGS] RATELIMITED TOO MANY REQUESTS, TRYING AGAIN")
            time.sleep(0.5)
            continue

        try:
            bought = bought.json()
        except:
            print(bought.reason)
            print(">> [LOGS] JSON DECODING ERROR WHILE TRYING TO BUY")
            continue

        if not bought["purchased"]:
            print(f">> [LOGS] FAILED BUYING LIMITED, TRYING AGAIN - {bought} - {data}")
        else:
            print(f">> [LOGS] SUCCESSFULLY PURCHASED LIMITED - {bought} - {data}")
            r.post(discordWebhook, data={"content": f">> [LOGS] PURCHASED FREE LIMITED - {bought} - {data}"})
            

        try:
            info = r.post("https://catalog.roblox.com/v1/catalog/items/details",
                      json={"items": [{"itemType": "Asset", "id": int(limited)}]},
                      headers={"x-csrf-token": x_token}, cookies={".ROBLOSECURITY": cookie}).json()["data"][0]
        except:
            print(f">> [LOGS] FAILED GETTING STOCK {info.text} - {info.reason}")
            left = 0

        if left == 0:
            print(">> [LOGS] COULD NOT BUY IN TIME SADLY")
            return


# Get collectible and product id for all the limiteds.
Thread(target=get_x_token).start()


while x_token == "":
    time.sleep(0.01)



cooldown = 60/(39/len(limiteds))-0.8
while 1:
    start = time.perf_counter()

    for limited in limiteds:
        try:
            info = r.post("https://catalog.roblox.com/v1/catalog/items/details",
                           json={"items": [{"itemType": "Asset", "id": int(limited)}]},
                           headers={"x-csrf-token": x_token}, cookies={".ROBLOSECURITY": cookie}).json()["data"][0]
        except KeyError:
            print(">> [LOGS] RATELIMITED WAITING FOR 60 SECONDS")
            time.sleep(60-int(datetime.datetime.now().second))
            continue

        if info.get("priceStatus", "") != "Off Sale":
            try:
                productid = r.post("https://apis.roblox.com/marketplace-items/v1/items/details",
                    json={"itemIds": [info["collectibleItemId"]]},
                    headers={"x-csrf-token": x_token}, cookies={".ROBLOSECURITY": cookie}).json()[0]["collectibleProductId"]

                buy(info, info["collectibleItemId"], productid)
            except:
                print(">> [LOGS] CAUGHT ERRROR")
                continue

    taken = time.perf_counter()-start
    if taken < cooldown:
        time.sleep(cooldown-taken)

    os.system("cls")
    print(">> [CREDITS] Made with love by noahrepublic, J3ldo, slourn, pompompurin, and duckyy.")
    print(">> [DISCORD] https://discord.gg/XX6qtbvkHG")
    print("Also to the people who hacked our server: your a bitch :)")
    print(">> [LOGS] CHECK DONE\n"
          f"TIME TAKEN: {round(time.perf_counter()-start, 3)}\n"
          f"IDEAL TIME: {round(cooldown, 3)}")
    
