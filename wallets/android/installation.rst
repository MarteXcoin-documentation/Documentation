.. meta::
   :description: How to install the MarteX wallet on your Android device
   :keywords: martex, mobile, wallet, android, installation, compile

.. _martex-android-installation:

Installation
============

Google Play
-----------

The easiest way to install the MarteX Wallet for Android is from the
Google Play Store. 

.. image:: images/google-play-badge.png
    :width: 250 px
    :target: https://play.google.com/store/apps/details?id=com.martexcoin.wallet

From APK
--------

Some Android phone do not have access to the Google Play Store because
the phone software, network provider or country may not allow it. You
can install the app manually by first enabling installation of external
sources (if you have not already done so) and then downloading and
installing an APK file. Follow these instructions:

#. Ensure your Android version is at least 4.0.3 by going to **Settings
   → About phone** and checking the version number.
#. Enable Unknown sources by going to **Settings → Security → Unknown
   sources**. Read and accept the warning.
#. Using your phone, download the latest version of the APK from `this
   link <https://play.google.com/store/apps/details?id=com.martexcoin.wallet>`_
   using a web site that `download apk files from google play <https://www.google.com/search?hl=en&q=download%20apk%20from%20google%20play>`_.
#. If you cannot use your phone to go online, download the APK using
   your PC instead and copy it to your phone using a cable or Bluetooth.
   You may need a file browser to find the copied file.

You can also install an APK file directly from your computer using the
Android Debug Bridge (ADB). Follow these instructions:

#. Ensure your Android version is at least 4.0.3 by going to **Settings
   → About phone** and checking the version number.
#. Ensure you have a copy of ADB on your PC. This is included in the
   Android `SDK Platform Tools
   <https://developer.android.com/studio/releases/platform-tools.html>`_
   for Mac, Windows or Linux.
#. Enable Unknown sources by going to **Settings → Security → Unknown
   sources**. Read and accept the warning.
#. Enable USB debugging by going to **Settings → Developer options → USB
   debugging**. If **Developer options** is not available, go to **About
   phone** instead, scroll down, and tap on the **Build number** seven
   times.
#. Using your PC, download the latest version of the APK from `this
   link <https://play.google.com/store/apps/details?id=com.martexcoin.wallet>`_
   using a web site that `download apk files from google play <https://www.google.com/search?hl=en&q=download%20apk%20from%20google%20play>`_.
#. Connect your phone to the PC, open a terminal/command prompt window
   and type::

     adb install <<path to .apk file>>


From source
-----------

In the future we will publish the source code of android wallet.
