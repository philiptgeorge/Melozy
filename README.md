# Melozy
#A simple solution to modern problem , simple python console application to listen distraction free song selection during Dopamine detox

import random

print("========================================")
print("           MELOZY MOOD MUSIC BOT        ")
print("======================================\n")
 
name = input("hey there! what's your name? ")
print(f"\nwelcome, {name}!")
print("this program suggests songs based on your mood.")
print("you just type your mood, and i'll give you the top 3 songs!")
print("each time you try the same mood, you might get different results \n")

print("available moods:")
print("1. romantic / romance / love")
print("2. party / fun / enjoy / joy")
print("3. happy / vibe")
print("4. sad / heartbreak / breakup / lonely / sadness")
print("5. relaxed / calm / peaceful / travel / chill\n")

songs = {
    "romantic": [
        "SAIYAARA - https://open.spotify.com/track/1D35BJlymlh6OLD75WupSF?si=p7duOCcuQKi_u5Nvpa7H0A",
        "HEERIYE - https://open.spotify.com/track/5PUXKVVVQ74C3gl5vKy9Li?si=OgWG1YqvSv2W6uwV47ZA_w",
        "CHALEYA - https://open.spotify.com/track/4nc6XiUze2Yh7wFueGOPv7?si=VwMhhHyxQ3W2LsMojrq1PQ",
        "VELLARIPRAVU - https://open.spotify.com/track/61jc2asnDN7jERanhOThJa?si=r6IEBYaORUG4wgEh0I0tXw",
        "ME TERA BOYFRIEND - https://open.spotify.com/track/5VAkPCJTE6tbyReo9J4IQj?si=prSgzz1qQuCgaGTCTpvBZg",
        "ISHQ HAI - https://open.spotify.com/track/3vCzLB6kS2lGcIpm1OOUsy?si=Trj45cnsSPed-IzlFoQ2Ew"
    ],
    "party": [
        "BADTAMEEZ DIL - https://open.spotify.com/track/4eu27jAU2bbnyHUC3G75U8?si=E9bHKzr7TLWGFkEXInaszQ",
        "CHIKNI CHAMELI - https://open.spotify.com/track/1NtUkEglWHG26BOqj3rPhQ?si=GeyoAU1yQzKpN7sQ3fkLzA",
        "SADI GALI - https://open.spotify.com/track/1tEto4JrqNmBZFH5uAiYqb?si=ECgXa9pjQlG5PgneovCGBg",
        "MAKE SOME NOISE FOR THE DESI BOYS - https://open.spotify.com/track/71s7tZo8OGlN3VXyURWLUr?si=SMEhdgsyQJyapaf8vMdOpQ",
        "BALAM PICHKARI - https://open.spotify.com/track/18e3XXYCv4Tx8uUl1mP3CN?si=OSZ2VRaUQfGUc3VuEOzDZA",
        "LUNGI DANCE - https://open.spotify.com/track/3VXh3jYTW3lTxtXRnu2TKP?si=4nunb4tfSU6UaNefNiXipQ"
    ],
    "happy": [
        "ILLUMINATI - https://open.spotify.com/track/1kFNFsAZ4iZy4vjBEtT12I?si=j9s3se2aR-SM-bUokzeDUQ",
        "ZOOBI DOOBI - https://open.spotify.com/track/5Sb1gWmNRelFDAMb6eiriW?si=XskVxMDXQGOKHcAngVp9nQ",
        "CHARACTER DHEELA - https://open.spotify.com/track/1r4oikmMdZZiGHkPA4hSoe?si=XjGVV7v1QiODVKLmCmYONw",
        "LATOO - https://open.spotify.com/track/4CuBg0h6kD85MPN8Ntq6Zr?si=fQTKP1S2SVSomHLey6408Q",
        "ZAALIMA - https://open.spotify.com/track/1J9vyEntJ79CppvgUxJs75?si=GXIMUE2DSUurAdhBNd3aeA",
        "TAUBA TAUBA - https://open.spotify.com/track/16kiQQ4BoLHDyj5W2fkfNK?si=JpY4NHnsSqS_72gyJw7tmQ"
    ],
    "sad": [
        "AGAR TUM SATH HO - https://open.spotify.com/track/2FCXQHugkoHE1K3tiDu8pu?si=5A7gjuL4T1OKpNzr78i7Ww",
        "TUM HI HO - https://open.spotify.com/track/56zZ48jdyY2oDXHVnwg5Di?si=LuTPgXbVRxm0Jn3pm_hvJg",
        "ENNA SONA - https://open.spotify.com/track/6bdpj89aYEBjhpsenXAsmO?si=fplA5-RUTQ6z2bcpwib86g",
        "CHANNA MEREYA - https://open.spotify.com/track/0H2iJVgorRR0ZFgRqGUjUM?si=s9IIB_vFTw-e0eM8vn1VSw",
        "KHO GAYA - https://open.spotify.com/track/2QophXhN2Ls2URfoPmiviC?si=wofAyQ9uS_SKMGhvUAVlpQ",
        "UYIRE - https://open.spotify.com/track/0vmxxVMfJN21J3xX2uqzkg?si=9oZipp7JT0qtcR9VEzDPiQ"
    ],
    "relaxed": [
        "SAMAJAVARAGAMANA - https://open.spotify.com/track/3j9DrRebdWK1jkpOw9FZUy?si=sDqKkPE8QL6RYo6r_xqKIQ",
        "GOD'S PLAN - https://open.spotify.com/track/6DCZcSspjsKoFjzjrWoCdn?si=Iw5SDiRMSvGXq_7Qsao0rA",
        "RABBA - https://open.spotify.com/track/1dZ0keYimkCuwRng7RI3BQ?si=rEgKZl9RRXidyepJaRD_XA",
        "PASOORI NU - https://open.spotify.com/track/6byRW2mzuc4nBTZ6TN6APu?si=YR2coAeHQO-vKqJBdmlszQ",
        "ONE LOVE - https://open.spotify.com/track/5ZLkihi6DVsHwDL3B8ym1t?si=mPuf_Um0SbmDcQBzp0kXew",
        "TUH HAI TOH - https://open.spotify.com/track/6egfWbtFFhMToV2DvmEzmo?si=bswHnnqkSMKG7NiHG3d9lQ"
    ]
}

aliases = {
    "romance": "romantic",                                   #aliases, adding alternative words to the main emotion.
    "love": "romantic",
    "fun": "party",
    "enjoy": "party",
    "joy": "party",
    "vibe": "happy",
    "heartbreak": "sad",
    "breakup": "sad",
    "lonely": "sad",
    "sadness": "sad",
    "calm": "relaxed",
    "peaceful": "relaxed",
    "travel": "relaxed",
    "chill": "relaxed"
}

while True:
    mood = input("\nenter your mood (e.g., happy, romantic, party, sad, relaxed) or type 'exit' to quit: ").lower()

    if mood == "exit":
        print(f"\ngoodbye, {name}! Hope you enjoyed the music! ")
        break

    if mood in aliases:
        mood = aliases[mood]

    if mood in songs:
        print(f"\nhere are 3 songs for your {mood} mood:\n")
        selected_songs = random.sample(songs[mood], 3)
        for song in selected_songs:
            print("-", song)
    else:
        print("sorry, I don't recognize that mood. try again!")
