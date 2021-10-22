---
description: Retrieve all tokens that are stored on a wallet address
---

# Get NFTs by address

{% swagger baseUrl="https://<chain>-azrael.arkane.network" path="/:walletAddress/tokens" method="get" summary="Get tokens by wallet address" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="walletAddress" type="string" %}
Address of the wallet
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
[
    {
        "type": "ERC_1155",
        "address": "0xaf791509b3e8a5bf1703918e457a2fdd50783319",
        "name": "CryptoPick",
        "symbol": "CP",
        "tokens": [
            {
                "tokenId": "14751",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/14751/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "16452",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/16452/metadata",
                "metadata": "{\"name\":\"Red Dragon\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/dragonred.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/dragonred.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/dragonred.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":50,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"epic\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "24936",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/24936/metadata",
                "metadata": "{\"name\":\"Rusty Steel Trencher\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/rusty_steel_trencher.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/rusty_steel_trencher.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/rusty_steel_trencher.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Industrial\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "14901",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/14901/metadata",
                "metadata": "{\"name\":\"Blockchain\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "16407",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/16407/metadata",
                "metadata": "{\"name\":\"Lobster\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/lobster.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/lobster.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/lobster.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "471",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/471/metadata",
                "metadata": "{\"name\":\"Fast Food\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "9451",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/9451/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "4321",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/4321/metadata",
                "metadata": "{\"name\":\"Crystal Ball\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "7204",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/7204/metadata",
                "metadata": "{\"name\":\"Anonymous\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/anonymous.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/anonymous.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/anonymous.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "25317",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/25317/metadata",
                "metadata": "{\"name\":\"Rusty Bronze Trencher\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/rusty_bronze_trencher.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/rusty_bronze_trencher.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/rusty_bronze_trencher.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Industrial\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "7702",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/7702/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "7701",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/7701/metadata",
                "metadata": "{\"name\":\"Blockchain\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "14101",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/14101/metadata",
                "metadata": "{\"name\":\"Blockchain\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "10612",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/10612/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "1108",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/1108/metadata",
                "metadata": "{\"name\":\"Fast Food\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "1105",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/1105/metadata",
                "metadata": "{\"name\":\"Lobster\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/lobster.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/lobster.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/lobster.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "11801",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/11801/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "8851",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/8851/metadata",
                "metadata": "{\"name\":\"Crystal Ball\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            }
        ]
    },
    {
        "type": "ERC_1155",
        "address": "0xd52a86110c9a7597a057ae2bb4f577b6cd42a639",
        "name": null,
        "symbol": null,
        "tokens": [
            {
                "tokenId": "55",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmUEq5MAnDGRwEMfJPFYvTLiBnKi7XYNTiHaP9cqQXkCZN",
                "metadata": "{\"name\":\"Emotional Animals 001 by Melowilo\",\"description\":\"The Emotional Animals NFT collection is a little fun project to celebrate the fact that furry, scaly, feathery, slimy and distinctly human type animals feel these strange things called ‘emotion’ rather frequently.  Via the magic of NFT, you can now own one or even more of these, at a very reasonable price, and thereby really, in actuality own your emotions.  I mean really... like provable on the blockchain really.  Find your Emotional Animals, own it, share it, or whatever, but most importantly... feel those emotions!  It's OK we all have them.   Emotional Animals 001 has 99 copies only. \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmSA2dQRHW2bEGVor4n7pKVCUxPszs9CkUigLqtX7oM6HA\",\"external_url\":\"https://twitter.com/nft_animals\"}"
            },
            {
                "tokenId": "80",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/Qmc6Jy1BtHmZG7NZ8qAn2Z53ZSD84VmJiWcqY4iWGjEYkK",
                "metadata": "{\"name\":\"WOLF\",\"description\":\"$WOLF logo series ERC-1155 X/5\",\"image\":\"https://gateway.pinata.cloud/ipfs/QmVKA2xgHFJfqt9h6aSTZYdq54Yyw3mNznLPjGYFzx9d9F\",\"external_url\":\"https://moonwolf.io\"}"
            },
            {
                "tokenId": "21",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmPWEoE77dn8vbRy9HVDZ8fXo1foii2e2Y5PzFTwXms3Zp",
                "metadata": "{\"name\":\"Choco paste\",\"description\":\"Lovely choco paste, hmmmmm\",\"image\":\"https://gateway.pinata.cloud/ipfs/QmYYK1y7Naj7HvY54N8rTuPYdbSu8vzweu32nhBAjqWNUi\",\"external_url\":\"https://arkane.market\"}"
            },
            {
                "tokenId": "66",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmQcyU7CD7KXFYLrJmLYPnif2Q5raaL5svLSdgDErDcMNA",
                "metadata": "{\"name\":\"Emotional Animals 002 by Melowilo\",\"description\":\"The Emotional Animals NFT collection is a little fun project to celebrate the fact that furry, scaly, feathery, slimy and distinctly human type animals feel these strange things called ‘emotion’ rather frequently. Via the magic of NFT, you can now own one or even more of these, at a very reasonable price, and thereby really, in actuality own your emotions. I mean really... like provable on the blockchain really. Find your Emotional Animals, own it, share it, or whatever, but most importantly... feel those emotions! It's OK we all have them. Emotional Animals 002 has 99 copies only.\",\"image\":\"https://gateway.pinata.cloud/ipfs/QmSMieKsxxh6Mph6tw5gdkpD5g81HHUCbc1TQrmGg8Dhfq\",\"external_url\":\"https://twitter.com/nft_animals\"}"
            }
        ]
    },
    {
        "type": "ERC_1155",
        "address": "0xa02d547512bb90002807499f05495fe9c4c3943f",
        "name": "Staked GHST-QUICK LP",
        "symbol": "stkGHST-QUICK",
        "tokens": [
            {
                "tokenId": "0",
                "balance": "1",
                "uri": "https://aavegotchi.com/metadata/0",
                "metadata": "{\"name\":\"[INVALID -- DO NOT BUY!!!] Ticket - Common\",\"description\":\"INVALID ON ETHEREUM, MOVED TO POLYGON\",\"image\":\"https://aavegotchi.com/images/tickets/ticket-common.svg\",\"external_url\":\"https://aavegotchi.com/item/ticket-common\",\"background_color\":\"5D24BF\",\"attributes\":[{\"trait_type\":\"Rarity\",\"value\":\"Common\"},{\"trait_type\":\"Price\",\"value\":\"50 FRENS\"}]}"
            }
        ]
    },
    {
        "type": "ERC_1155",
        "address": "0xfd1dbd4114550a867ca46049c346b6cd452ec919",
        "name": null,
        "symbol": null,
        "tokens": [
            {
                "tokenId": "210",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmeBRbKwAZZhgNbqp9YN9BzzHnsQYsNDWXqncD7ZGJKUmN",
                "metadata": "{\"name\":\"Elon #2\",\"description\":\"     \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmcNUWJQ8EtB2v6a879oD7BTVANZBteE8PZyitStJjCaLs\",\"external_url\":\"\"}"
            },
            {
                "tokenId": "165",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmPAj8SjnxwgayiwzM1dKWTzJa3bmZYjDJHnLAyC1dAd9k",
                "metadata": "{\"name\":\"Drive-Thru Menu\",\"description\":\"    \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmTM1QfxyVF84Amb3XE1KG5GsGevDbz9X69HY2pZDVNmsV\",\"external_url\":\"\"}"
            },
            {
                "tokenId": "168",
                "balance": "2",
                "uri": "https://gateway.pinata.cloud/ipfs/Qmf4pXsfRWBa4kkBU6xvriscKYzbmWNENoWn4T4iTZ47GH",
                "metadata": "{\"name\":\"Fly Fries\",\"description\":\"    \",\"image\":\"https://gateway.pinata.cloud/ipfs/Qma4mToEZTZNTpL7tbzhzXjMvDdvuc1tEvv86TfaPrffRc\",\"external_url\":\"\"}"
            },
            {
                "tokenId": "166",
                "balance": "2",
                "uri": "https://gateway.pinata.cloud/ipfs/QmacqoMzrCfmHzFBKLFVYUNjdP5ypQJKoPZmdYetmTWsbx",
                "metadata": "{\"name\":\"Pop!\",\"description\":\"     \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmVDH1j8ZNfzHUM2uWQMRcdKJ5iwWfEnQKK9S2xcrzXG7L\",\"external_url\":\"\"}"
            }
        ]
    }
]
```
{% endswagger-response %}
{% endswagger %}

## Example

#### Request

```javascript
https://matic-azrael.arkane.network/0x9d9376EEbFE3443544d3654f7aD272f0A31D8152/tokens
```

#### Response

```javascript
[
    {
        "type": "ERC_1155",
        "address": "0xaf791509b3e8a5bf1703918e457a2fdd50783319",
        "name": "CryptoPick",
        "symbol": "CP",
        "tokens": [
            {
                "tokenId": "14751",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/14751/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "16452",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/16452/metadata",
                "metadata": "{\"name\":\"Red Dragon\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/dragonred.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/dragonred.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/dragonred.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":50,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"epic\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "24936",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/24936/metadata",
                "metadata": "{\"name\":\"Rusty Steel Trencher\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/rusty_steel_trencher.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/rusty_steel_trencher.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/rusty_steel_trencher.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Industrial\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "14901",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/14901/metadata",
                "metadata": "{\"name\":\"Blockchain\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "16407",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/16407/metadata",
                "metadata": "{\"name\":\"Lobster\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/lobster.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/lobster.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/lobster.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "471",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/471/metadata",
                "metadata": "{\"name\":\"Fast Food\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "9451",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/9451/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "4321",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/4321/metadata",
                "metadata": "{\"name\":\"Crystal Ball\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "7204",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/7204/metadata",
                "metadata": "{\"name\":\"Anonymous\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/anonymous.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/anonymous.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/anonymous.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "25317",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/25317/metadata",
                "metadata": "{\"name\":\"Rusty Bronze Trencher\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/rusty_bronze_trencher.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/rusty_bronze_trencher.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/rusty_bronze_trencher.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Industrial\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "7702",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/7702/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "7701",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/7701/metadata",
                "metadata": "{\"name\":\"Blockchain\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "14101",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/14101/metadata",
                "metadata": "{\"name\":\"Blockchain\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/pipe/blockchain.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Pipe\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "10612",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/10612/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "1108",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/1108/metadata",
                "metadata": "{\"name\":\"Fast Food\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/fastfood.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "1105",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/1105/metadata",
                "metadata": "{\"name\":\"Lobster\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/lobster.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/lobster.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/lobster.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":100,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"rare\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Genesis\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "11801",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/11801/metadata",
                "metadata": "{\"name\":\"PPK 007\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/claws/ppk_007.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Claws\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            },
            {
                "tokenId": "8851",
                "balance": "1",
                "uri": "https://metadata.arkane.network/api/apps/cb3383c2-1cb0-4707-a481-98b553e2ad0a/contracts/15/tokens/8851/metadata",
                "metadata": "{\"name\":\"Crystal Ball\",\"description\":\"\",\"image\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imagePreview\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"imageThumbnail\":\"https://cryptopick.net/images/avatars/parts/base/crystal_ball.svg\",\"backgroundColor\":\"#002d30\",\"background_color\":\"#002d30\",\"animationUrls\":[],\"maxSupply\":200,\"attributes\":[{\"type\":\"property\",\"name\":\"Part\",\"value\":\"Base\",\"traitType\":\"Part\",\"trait_type\":\"Part\"},{\"type\":\"property\",\"name\":\"Scarcity\",\"value\":\"common\",\"traitType\":\"Scarcity\",\"trait_type\":\"Scarcity\"},{\"type\":\"property\",\"name\":\"Collection\",\"value\":\"Community Contest #1\",\"traitType\":\"Collection\",\"trait_type\":\"Collection\"}],\"contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"asset_contract\":{\"address\":\"0xaf791509b3e8a5bf1703918e457a2fdd50783319\",\"name\":\"CryptoPick\",\"symbol\":\"CP\",\"description\":\"NFTs associated to CryptoPick, a market prediction game that rewards players in ETH, NFTs, and more while unlocking valuable trading insights.\",\"media\":[],\"type\":\"ERC_1155\"},\"fungible\":false}"
            }
        ]
    },
    {
        "type": "ERC_1155",
        "address": "0xd52a86110c9a7597a057ae2bb4f577b6cd42a639",
        "name": null,
        "symbol": null,
        "tokens": [
            {
                "tokenId": "55",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmUEq5MAnDGRwEMfJPFYvTLiBnKi7XYNTiHaP9cqQXkCZN",
                "metadata": "{\"name\":\"Emotional Animals 001 by Melowilo\",\"description\":\"The Emotional Animals NFT collection is a little fun project to celebrate the fact that furry, scaly, feathery, slimy and distinctly human type animals feel these strange things called ‘emotion’ rather frequently.  Via the magic of NFT, you can now own one or even more of these, at a very reasonable price, and thereby really, in actuality own your emotions.  I mean really... like provable on the blockchain really.  Find your Emotional Animals, own it, share it, or whatever, but most importantly... feel those emotions!  It's OK we all have them.   Emotional Animals 001 has 99 copies only. \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmSA2dQRHW2bEGVor4n7pKVCUxPszs9CkUigLqtX7oM6HA\",\"external_url\":\"https://twitter.com/nft_animals\"}"
            },
            {
                "tokenId": "80",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/Qmc6Jy1BtHmZG7NZ8qAn2Z53ZSD84VmJiWcqY4iWGjEYkK",
                "metadata": "{\"name\":\"WOLF\",\"description\":\"$WOLF logo series ERC-1155 X/5\",\"image\":\"https://gateway.pinata.cloud/ipfs/QmVKA2xgHFJfqt9h6aSTZYdq54Yyw3mNznLPjGYFzx9d9F\",\"external_url\":\"https://moonwolf.io\"}"
            },
            {
                "tokenId": "21",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmPWEoE77dn8vbRy9HVDZ8fXo1foii2e2Y5PzFTwXms3Zp",
                "metadata": "{\"name\":\"Choco paste\",\"description\":\"Lovely choco paste, hmmmmm\",\"image\":\"https://gateway.pinata.cloud/ipfs/QmYYK1y7Naj7HvY54N8rTuPYdbSu8vzweu32nhBAjqWNUi\",\"external_url\":\"https://arkane.market\"}"
            },
            {
                "tokenId": "66",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmQcyU7CD7KXFYLrJmLYPnif2Q5raaL5svLSdgDErDcMNA",
                "metadata": "{\"name\":\"Emotional Animals 002 by Melowilo\",\"description\":\"The Emotional Animals NFT collection is a little fun project to celebrate the fact that furry, scaly, feathery, slimy and distinctly human type animals feel these strange things called ‘emotion’ rather frequently. Via the magic of NFT, you can now own one or even more of these, at a very reasonable price, and thereby really, in actuality own your emotions. I mean really... like provable on the blockchain really. Find your Emotional Animals, own it, share it, or whatever, but most importantly... feel those emotions! It's OK we all have them. Emotional Animals 002 has 99 copies only.\",\"image\":\"https://gateway.pinata.cloud/ipfs/QmSMieKsxxh6Mph6tw5gdkpD5g81HHUCbc1TQrmGg8Dhfq\",\"external_url\":\"https://twitter.com/nft_animals\"}"
            }
        ]
    },
    {
        "type": "ERC_1155",
        "address": "0xa02d547512bb90002807499f05495fe9c4c3943f",
        "name": "Staked GHST-QUICK LP",
        "symbol": "stkGHST-QUICK",
        "tokens": [
            {
                "tokenId": "0",
                "balance": "1",
                "uri": "https://aavegotchi.com/metadata/0",
                "metadata": "{\"name\":\"[INVALID -- DO NOT BUY!!!] Ticket - Common\",\"description\":\"INVALID ON ETHEREUM, MOVED TO POLYGON\",\"image\":\"https://aavegotchi.com/images/tickets/ticket-common.svg\",\"external_url\":\"https://aavegotchi.com/item/ticket-common\",\"background_color\":\"5D24BF\",\"attributes\":[{\"trait_type\":\"Rarity\",\"value\":\"Common\"},{\"trait_type\":\"Price\",\"value\":\"50 FRENS\"}]}"
            }
        ]
    },
    {
        "type": "ERC_1155",
        "address": "0xfd1dbd4114550a867ca46049c346b6cd452ec919",
        "name": null,
        "symbol": null,
        "tokens": [
            {
                "tokenId": "210",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmeBRbKwAZZhgNbqp9YN9BzzHnsQYsNDWXqncD7ZGJKUmN",
                "metadata": "{\"name\":\"Elon #2\",\"description\":\"     \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmcNUWJQ8EtB2v6a879oD7BTVANZBteE8PZyitStJjCaLs\",\"external_url\":\"\"}"
            },
            {
                "tokenId": "165",
                "balance": "1",
                "uri": "https://gateway.pinata.cloud/ipfs/QmPAj8SjnxwgayiwzM1dKWTzJa3bmZYjDJHnLAyC1dAd9k",
                "metadata": "{\"name\":\"Drive-Thru Menu\",\"description\":\"    \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmTM1QfxyVF84Amb3XE1KG5GsGevDbz9X69HY2pZDVNmsV\",\"external_url\":\"\"}"
            },
            {
                "tokenId": "168",
                "balance": "2",
                "uri": "https://gateway.pinata.cloud/ipfs/Qmf4pXsfRWBa4kkBU6xvriscKYzbmWNENoWn4T4iTZ47GH",
                "metadata": "{\"name\":\"Fly Fries\",\"description\":\"    \",\"image\":\"https://gateway.pinata.cloud/ipfs/Qma4mToEZTZNTpL7tbzhzXjMvDdvuc1tEvv86TfaPrffRc\",\"external_url\":\"\"}"
            },
            {
                "tokenId": "166",
                "balance": "2",
                "uri": "https://gateway.pinata.cloud/ipfs/QmacqoMzrCfmHzFBKLFVYUNjdP5ypQJKoPZmdYetmTWsbx",
                "metadata": "{\"name\":\"Pop!\",\"description\":\"     \",\"image\":\"https://gateway.pinata.cloud/ipfs/QmVDH1j8ZNfzHUM2uWQMRcdKJ5iwWfEnQKK9S2xcrzXG7L\",\"external_url\":\"\"}"
            }
        ]
    }
]
```
