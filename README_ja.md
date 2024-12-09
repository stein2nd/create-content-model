<!-- 
# Create Content Model
 -->
# Create Content Model

<!-- 
_Define custom post types & fields in the Block Editor._
 -->
_ブロックエディターで、カスタム投稿タイプとフィールドを定義します。_

<!-- 
WordPress.com’s experimental Create Content Model plugin transforms the way custom post types and custom fields are created and managed in WordPress by making use of the latest core features to bring content modeling into the Block Editor. Additionally, the created data model and data entry UI can be exported as a standalone, maintenance-free plugin.
 -->
WordPress.com の実験的な Create Content Model プラグインは、最新のコア機能を利用してブロックエディタにコンテンツモデリングを導入することで、WordPress でカスタム投稿タイプやカスタムフィールドを作成・管理する方法を変革します。さらに、作成されたデータモデルとデータ入力 UI は、スタンドアロンでメンテナンスフリーのプラグインとしてエクスポートできます。

<!-- 
[![Try in WordPress Playground](https://img.shields.io/badge/Try%20in%20WordPress%20Playground-blue?style=for-the-badge)](https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/Automattic/create-content-model/trunk/blueprint.json)
 -->
[![WordPress Playground で試す](https://img.shields.io/badge/Try%20in%20WordPress%20Playground-blue?style=for-the-badge)](https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/Automattic/create-content-model/trunk/blueprint.json)

<!-- 
You can also test out the plugin locally with [Studio](https://developer.wordpress.com/studio/?utm_source=github&utm_medium=readme&utm_campaign=create-content-model)! Check out the [Get Started](/get-started.md#test-locally-with-studio) guide for details.
 -->
[Studio](https://developer.wordpress.com/studio/?utm_source=github&utm_medium=readme&utm_campaign=create-content-model)を使ってローカルでプラグインをテストすることもできます ! 詳しくは、[始めよう](/get-started.md#test-locally-with-studio)ガイドをご覧ください。

<!-- 
https://github.com/user-attachments/assets/723a973a-eb92-4b71-9f64-ac269d0f9861
 -->
https://github.com/user-attachments/assets/723a973a-eb92-4b71-9f64-ac269d0f9861

<!-- 
For a more thorough introduction, check out Brian Coord's [Custom fields and post types inside the block editor livestream](https://www.youtube.com/watch?v=VLB3OkgNOTs).
 -->
より詳細な紹介は、Brian Coord の[ブロックエディタ内のカスタムフィールドと投稿タイプ ライブストリーム](https://www.youtube.com/watch?v=VLB3OkgNOTs)をご覧ください。

<!-- 
## Getting Started
 -->
## はじめに

<!-- 
Find detailed instructions on creating your content model using this plugin in the [Get Started](/get-started.md) guide.
 -->
このプラグインを使用してコンテンツモデルを作成する詳細な手順は、[始めよう](/get-started.md)ガイドをご覧ください。

<!-- 
[![Download Latest Release](https://img.shields.io/badge/Download%20Latest%20Release-blue?style=for-the-badge)](https://github.com/Automattic/create-content-model/releases/latest/download/create-content-model.zip)
 -->
[![最新リリースをダウンロードする](https://img.shields.io/badge/Download%20Latest%20Release-blue?style=for-the-badge)](https://github.com/Automattic/create-content-model/releases/latest/download/create-content-model.zip)

<!-- 
## About
 -->
## About

<!-- 
Our team at WordPress.com is excited to share our recent prototyping efforts on game changing approaches to custom content creation. 
 -->
WordPress.com の我々のチームは、カスタムコンテンツ作成への大きな変革をもたらすアプローチに関する、最近のプロトタイピングの取り組みを共有できることを嬉しく思っています。

<!-- 
The Create Content Model plugin builds upon our custom post types project at the [CloudFest Hackathon in 2024](https://wordpress.com/blog/2024/04/15/custom-post-types-wordpress-admin/?utm_source=github&utm_medium=readme&utm_campaign=create-content-model). We’ve leveraged core functionality, like [block bindings](https://make.wordpress.org/core/2024/03/06/new-feature-the-block-bindings-api/) and [block variations](https://developer.wordpress.org/block-editor/reference-guides/block-api/block-variations/), to create a new paradigm for creating and managing custom post types and custom fields in WordPress.
 -->
Create Content Model プラグインは、[CloudFest ハッカソン in 2024](https://wordpress.com/blog/2024/04/15/custom-post-types-wordpress-admin/?utm_source=github&utm_medium=readme&utm_campaign=create-content-model)でのカスタム投稿タイププロジェクトがベースになって構築されています。[ブロック・バインディング](https://make.wordpress.org/core/2024/03/06/new-feature-the-block-bindings-api/)や[ブロック・バリエーション](https://developer.wordpress.org/block-editor/reference-guides/block-api/block-variations/)などのコア機能を活用して、WordPress でカスタム投稿タイプやカスタムフィールドを作成・管理するための新しいパラダイムを作りました。

<!-- 
Unlike existing custom post type and custom field plugins, our plugin takes a native approach by putting the creation and management of these elements directly in the WordPress Block Editor. Using the Block Bindings API, `post_meta` fields are bound to block attributes. Block variations are created from each bound block for use in front-end template layouts. The result is an extremely intuitive workflow for both the setup of custom post types and fields and their usage in front-end templating.
 -->
既存のカスタム投稿タイプやカスタムフィールドのプラグインとは異なり、私たちのプラグインは、これらの要素の作成と管理を WordPress ブロックエディタに直接置くことで、ネイティブなアプローチを採用しています。ブロック・バインディング API を使って、`post_meta` フィールドがブロック属性にバインドされます。ブロック・バリエーションは、フロントエンドのテンプレートレイアウトで使用するために、バインドされた各ブロックから作成されます。その結果、カスタム投稿タイプやカスタムフィールドのセットアップと、フロントエンドのテンプレートレイアウトでの利用の両方において、非常に直感的なワークフローが実現します。

<!-- 
A key feature of the Create Content Model plugin is the export of a locked custom data model and a data entry UI. Developers can generate and reuse the same content models on multiple sites without ongoing plugin maintenance or costs. They can hand off fully functional sites with locked custom post types and fields, ready for clients to populate the content.
 -->
Create Content Model プラグインの主要機能は、ロックされたカスタムデータモデルとデータ入力 UI のエクスポートです。開発者は、継続的なプラグインのメンテナンスやコストをかけることなく、複数のサイトで同じコンテンツモデルを生成して再利用できます。開発者は、ロックされたカスタム投稿タイプとカスタムフィールドを持つ、完全に機能するサイトを提供でき、クライアントがコンテンツを入力する準備ができます。

<!-- 
## Development
 -->
## 開発

<!-- 
* Run `npm install` to install the dependencies
* Run `npm run dev-server` to start the local WordPress server
* In a new terminal window, run `npm start` to start the JavaScript bundler watcher
 -->
* `npm install` を実行して、依存関係をインストールします。
* `npm run dev-server` を実行して、ローカルの WordPress サーバーを起動します。
* 新しいターミナルウィンドウで `npm start` を実行して、JavaScript バンドラー・ウォッチャーを起動します。

<!-- 
### Bundling
 -->
### バンドル

<!-- 
Run `npm run plugin-zip` to create a zip file of the plugin. This will automatically bundle the JavaScript files.
 -->
`npm run plugin-zip` を実行して、プラグインの zip ファイルを作成します。これで JavaScript ファイルが自動的にバンドルされます。

<!-- 
### Creating a new release
 -->
### 新規リリースの作成

<!-- 
Create a new release by filling the form on [this page](https://github.com/Automattic/create-content-model/releases/new).
 -->
[このページ](https://github.com/Automattic/create-content-model/releases/new)のフォームに記入して、新規リリースを作成してください。

<!-- 
The release title and tag ("Choose a tag" selectbox, above the title) should be in the Semver format (`major.minor.patch`).
 -->
リリースのタイトルとタグ (タイトルの上にある「Choose a tag」セレクトボックス) は、Semver フォーマット (`major.minor.patch`) に従ってください。

<!-- 
The release description should be a list of bullet points of the most meaningful changes. You can copy the commit title from the merged PRs.
 -->
リリースの説明は、最も意味のある変更点を箇条書きにしたリストにしてください。コミットタイトルは、マージされた Pull Request からコピーできます。

<!-- 
After clicking "Publish release," a [GitHub workflow](https://github.com/Automattic/create-content-model/blob/trunk/.github/workflows/release.yml) will bundle the plugin and export the release artifact.
 -->
「Publish release」をクリックすると、[GitHub ワークフロー](https://github.com/Automattic/create-content-model/blob/trunk/.github/workflows/release.yml)がプラグインをバンドルし、リリース成果物をエクスポートします。

<!-- 
## Contribute & Contact
 -->
## 貢献 & 連絡先

<!-- 
Want to help us move this concept forward?
 -->
このコンセプトを前進させるために、力を貸していただけませんか?

<!-- 
Feel free to open an issue in the repo to discuss your proposed improvement. Pull requests are welcome for bug fixes and enhancements.
 -->
あなたの改善案について議論するために、リポジトリに issue を自由に開いてください。バグフィックスや機能強化のための Pull Request も歓迎します。

<!-- 
We built this as a prototype and may invest into it further based on level of interest. Our near term vision is outlined in this [roadmap issue](https://github.com/Automattic/create-content-model/issues/77).
 -->
私たちはこれをプロトタイプとして構築し、関心の度合いに応じてさらに投資する可能性があります。私たちの近い将来のビジョンは、この[ロードマップ issue](https://github.com/Automattic/create-content-model/issues/77)に概説されています。

<!-- 
## Licensing
 -->
## ライセンス

<!-- 
[GNU General Public License](/LICENSE.md)
 -->
[GNU 一般公衆ライセンス](/LICENSE.md)

<!-- 
## Credits & Acknowledgements
 -->
## クレジット & 謝辞

<!-- 
We’d like to thank the team at WordPress.com who made this project possible: [Luis Felipe Zaguini](https://github.com/zaguiini), [Candy Tsai](https://github.com/candy02058912), [Autumn Fjeld](https://github.com/autumnfjeld), [Brian Coords](https://github.com/bacoords), [Daniel Bachhuber](https://github.com/danielbachhuber).
 -->
このプロジェクトを可能にしてくれたWordPress.comのチームに感謝します: [Luis Felipe Zaguini](https://github.com/zaguiini)、[Candy Tsai](https://github.com/candy02058912)、[Autumn Fjeld](https://github.com/autumnfjeld)、[Brian Coords](https://github.com/bacoords)、[Daniel Bachhuber](https://github.com/danielbachhuber)。

<!-- 
## Stay in the Loop with WordPress.com
 -->
## WordPress.com で常に最新の情報を入手する

<!-- 
Follow us:
 -->
フォローしてください:

<!-- 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/showcase/wordpress.com)
 -->
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/showcase/wordpress.com)

<!-- 
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/wordpressdotcom)
 -->
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/wordpressdotcom)

<!-- 
[![image](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/wordpressdotcom)
 -->
[![image](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/wordpressdotcom)

<!-- Later we can add developers newsletter -->

<!-- 
And while you’re at it, check out our [WordPress hosting solution for developers](https://wordpress.com/hosting?utm_source=github&utm_medium=readme&utm_campaign=create-content-model) and [our agency program](https://wordpress.com/for-agencies/?utm_source=github&utm_medium=readme&utm_campaign=create-content-model).
 -->
ついでに、[開発者向け WordPress ホスティング・ソリューション](https://wordpress.com/hosting?utm_source=github&utm_medium=readme&utm_campaign=create-content-model)や[代理店プログラム](https://wordpress.com/for-agencies/?utm_source=github&utm_medium=readme&utm_campaign=create-content-model)もチェックしてみてください。