# Genshin

Genshin Integration allows you to connect your game account and use it with Mahiru.

???+ Warning "Warning"

    Hoyoverse do not provide any official way to connect your HoYoLab/Genshin account 
    to third-party applications. That's why most methods used by Mahiru were obtained 
    via reverse-engineering of HoYoLab API. But as long as you don't give your personal 
    data to anyone and don't spam requests through Mahiru, your account is completely safe,
    because requests made by Mahiru are absolutely same as those that you make in a regular 
    browser when browsing HoYoLab.

## Connecting your account

### How

<div class="annotate" markdown>
1. Open **Dashboard** and navigate to **Genshin Impact** integration.
2. Click on **«Connect HoYoLab account»**.
3. Enter your HoYoLab account name/email and password. (1)
4. Solve captcha.
5. Select your game account. (2)
6. Enjoy genshin features!
</div>

1.  Your account name and password are safely encrypted using OpenSSL. No one can decrypt them except Mahiru.
2.  You can switch to another account in the feature without a need to log in again. See [Switching game account](#switching-game-account).

### Why

Because all requests to Hoyolab must be made with your cookies. This also allows us to access your Genshin data even if it is not public on HoYoLab.

## Switching game account

If you want to switch server, for example, from **Europe** to **Asia**, you can do this without a need to log in again:

1. Open you **Genshin Profile** in **Dashboard**.
2. Click **«:octicons-kebab-horizontal-24:»** in the right top corner and tap on **«Switch account»**.
3. Select another account on another server.
4. Wait till Mahiru loads your new account and you are done!

## Settings

You can open Genshin settings by clicking **«:octicons-kebab-horizontal-24:»** in the right top corner of your **Genshin Profile** page and tapping on **«Settings»**.

### Appearance

#### Theme

The theme used in all Genshin images that you view. You can set either `light` or `dark` theme. By default, your device theme is set once you connect your Genshin account.

### Automation

#### Daily Check-in

???+ Warning "Warning"

    This feature does not work right now because Hoyoverse implemented CAPTCHA for daily check-in.
    We will add a way to deal with it in the future, but it will most likely be either a paid
    feature or a manually solvable CAPTCHA.

Automatically claims HoYoLab check-in reward every day.

#### Redeem Codes

Automatically redeems global codes like the ones from update streams.

### Display to others

#### Profile

Whether others are able to view your profile.

#### Characters

Whether others are able to view your characters.

#### Spiral Abyss

Whether others are able to view your Spiral Abyss statistics.

#### Teapot

Whether others are able to view your teapot statistics.

#### TCG

Whether others are able to view your TCG statistics.

#### Exploration progress

Whether others are able to view your exploration progress.