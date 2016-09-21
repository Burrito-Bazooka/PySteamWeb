Requirements
============

* Python 3.5+
* pyCrypto
* aiohttp

Installation
===========

* pip3 install pysteamweb

Usage
=====

.. code-block:: python

    >>> import asyncio
    >>> from pysteamweb import SteamWebBase
    >>>
    >>> async def main():
    >>>     async with SteamWebBase(
    >>>         username='<Steam login>',
    >>>         password='<Steam password>',
    >>>     ) as s:
    >>>         print('login successful')
    >>>         print(await s.session.send_session(url='http://steamcommunity.com/profiles/{}/edit'.format(s.steam_id), is_post=False))
    >>>
    >>>
    >>> if __name__ == '__main__':
    >>>     loop = asyncio.get_event_loop()
    >>>     loop.run_until_complete(main())
    >>>     loop.close()


Demos
=====

Look at demo folder
