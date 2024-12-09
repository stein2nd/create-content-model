<!-- 
# Get Started
 -->
# 始めよう

<!-- 
Start leveraging the latest WordPress core features with WordPress.com’s experimental Create Content Model plugin. 
 -->
WordPress.com の実験的な Create Content Model プラグインで、WordPress の最新コア機能の活用を始めましょう。

<!-- 
Create custom post types and custom fields directly in the Block Editor, and then export your data model and data entry UI as a standalone, maintenance-free plugin. Everything you build is using core WordPress functionality, so you can run the future-proof plugin or you can use filters and hooks to extend and adapt your data model.
 -->
ブロックエディタで直接カスタム投稿タイプやカスタムフィールドを作成し、その後、あなたのデータモデルとデータ入力 UI をスタンドアロンでメンテナンスフリーなプラグインとしてエクスポートします。構築したものはすべて WordPress のコア機能を使用しているため、将来性のあるプラグインを実行することも、フィルターやフックを使用してあなたのデータモデルを拡張したり適応させたりもできます。

<!-- 
To get started with the Create Content Model plugin, [download the latest release](https://github.com/Automattic/create-content-model/releases/latest/download/create-content-model.zip), [launch our WordPress Playground Blueprint](https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/Automattic/create-content-model/trunk/blueprint.json), or [test locally with Studio](#test-locally-with-studio).
 -->
Create Content Model プラグインを始めるには、[最新リリースをダウンロード](https://github.com/Automattic/create-content-model/releases/latest/download/create-content-model.zip)し、[WordPress Playground Blueprint を起動](https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/Automattic/create-content-model/trunk/blueprint.json)または[Studio でローカル・テスト](#test-locally-with-studio)してください。

<!-- 
https://github.com/user-attachments/assets/09b449f0-4398-4037-ba07-820c76407d7d
 -->
https://github.com/user-attachments/assets/09b449f0-4398-4037-ba07-820c76407d7d

<!-- 
## Creating a content model
 -->
## コンテンツモデルの作成

<!-- 
A content model is a custom post type that you can register and build directly in WordPress core. As you design it, you select which blocks are editable and can add custom fields.
 -->
コンテンツモデルは、WordPress コアに直接登録して構築できるカスタム投稿タイプです。デザインしながら、編集可能なブロックを選択し、カスタムフィールドを追加できます。

<!-- 
Creating a new content model includes:
 -->
新規コンテンツモデルの作成には、以下が含まれます:

<!-- 
1. Registering a new post type.
2. Designing the frontend template for your new post type and selecting which blocks in the template are editable by adding new “Bindings.”
3. Adding custom fields to your post to collect additional data.
 -->
1. 新規投稿タイプを登録する。
2. あなたの新規投稿タイプのフロントエンド・テンプレートをデザインし、新規「バインディング」を追加することによって、テンプレート内のどのブロックを編集可能にするかを選択する。
3. 追加データを収集するために、あなたの投稿にカスタムフィールドを追加する。

<!-- 
*Note that custom taxonomy support is on the [roadmap](https://github.com/Automattic/create-content-model/issues/77).*
 -->
*なお、カスタム・タクソノミーのサポートは、[ロードマップ](https://github.com/Automattic/create-content-model/issues/77)にあります*

<!-- 
### Register the post type 
 -->
### 投稿タイプの登録

<!-- 
From the Content Models page:
 -->
コンテンツモデルのページから:

<!-- 
1. Click **Add New Model**.
2. Name your content model.
3. Manage the post type settings using the sidebar panel: Singular Label, Plural Label, Icon Name
 -->
1. **Add New Model** をクリックします。
2. コンテンツモデルに名前を付けます。
3. サイドバーパネルで、投稿タイプの設定を管理します: 単数形ラベル、複数形ラベル、アイコン名。

<!-- 
![data-model-post-type-labels](https://github.com/user-attachments/assets/9369283f-d8d9-4040-8ec3-722ef8b9d0ff)
 -->
![data-model-post-type-labels](https://github.com/user-attachments/assets/9369283f-d8d9-4040-8ec3-722ef8b9d0ff)

<!-- 
### Design the frontend template for your new post type
 -->
### 新規投稿タイプが表示されるフロントエンド・テンプレートのデザイン

<!-- 
Once you’ve created the post type, you can start designing the template.
 -->
投稿タイプを作成したら、テンプレートのデザインを始めることができます。

<!-- 
As you add blocks to the template, they will not be editable by default. You’ll need to select which blocks include dynamic (aka editable) data by selecting **Add Binding** in the block sidebar controls. 
 -->
テンプレートにブロックを追加しても、デフォルトでは編集可能ではありません。ブロック・サイドバーのコントロールで **Add Binding** を選択して、どのブロックが動的な (つまり編集可能な) データを含むかを選択する必要があります。

<!-- 
Once a block is “bound,” it will be editable in the future, and any data entered will be automatically stored as postmeta, meaning you can use that data in different templates or query loops, view it in the REST API, bulk manage it via the database, and much more. 
 -->
一度ブロックが「バインド」されると、そのブロックは将来編集可能になり、入力されたデータは自動的に postmeta として保存されます。つまり、そのデータを別のテンプレートや query loop で使用したり、REST API で表示したり、データベースで一括管理したり、その他いろいろなことができるようになります。

<!-- 
![data-model-add-binding](https://github.com/user-attachments/assets/7a93ce88-f241-4017-bc01-1ecb472164b1)
 -->
![data-model-add-binding](https://github.com/user-attachments/assets/7a93ce88-f241-4017-bc01-1ecb472164b1)

<!-- 
If you have the [Gutenberg plugin](https://wordpress.org/plugins/gutenberg/) and enable the "Block Binding UI" experiment enabled, you can view and use your custom fields registered as postmeta when you manually bind an attribute.
 -->
[Gutenberg プラグイン](https://wordpress.org/plugins/gutenberg/)を使用し、「ブロック・バインディング UI」実験を有効にしている場合、手動で属性をバインディングすると、postmeta として登録されたカスタムフィールドを表示して使用できます。

<!-- 
Since we’re using core WordPress’ [Block Bindings API](https://make.wordpress.org/core/2024/03/06/new-feature-the-block-bindings-api/), the only blocks that are currently supported are the [Paragraph](https://wordpress.org/documentation/article/paragraph-block/), [Heading](https://wordpress.org/documentation/article/heading-block/), [Image](https://wordpress.org/documentation/article/image-block/), and [Buttons](https://wordpress.org/documentation/article/buttons-block/) blocks.
 -->
WordPress のコアである[ブロック・バインディング API](https://make.wordpress.org/core/2024/03/06/new-feature-the-block-bindings-api/)を使用しているため、現在のところ対応しているブロックは[段落](https://wordpress.org/documentation/article/paragraph-block/)、[見出し](https://wordpress.org/documentation/article/heading-block/)、[画像](https://wordpress.org/documentation/article/image-block/)、[ボタン](https://wordpress.org/documentation/article/buttons-block/)のみです。

<!-- 
### Rich content areas: the Group block
 -->
### リッチ・コンテンツエリア: グループ・ブロック

<!-- 
This tool also allows you to bind the [Group](https://wordpress.org/documentation/article/group-block/) block to a post meta field, which creates a “rich text” or WYSIWYG area in your template where multiple blocks can be used. A bound group block will store its contents in a post meta field, or you can map it directly to the `post_content` attribute. 
 -->
このツールでは、[グループ](https://wordpress.org/documentation/article/group-block/)ブロックを投稿メタフィールドにバインドできます。これにより、テンプレート内に複数のブロックを使用できる「リッチテキスト」または WYSIWYG エリアを作成できます。バインドされたグループブロックは、その内容を投稿メタフィールドに保存したり、`post_content` 属性に直接マッピングしたりできます。

<!-- 
![data-model-attribute-bindings](https://github.com/user-attachments/assets/6dfd750a-315b-46cd-ac73-4426b8e7a54f)
 -->
![data-model-attribute-bindings](https://github.com/user-attachments/assets/6dfd750a-315b-46cd-ac73-4426b8e7a54f)

<!-- 
## Your data model and custom fields
 -->
## あなたのデータモデルとカスタムフィールド

<!-- 
All of your bound blocks will save their content to post meta fields, so you can redesign, remix, and filter your content model in the future and without losing the integrity of your data. Open the Post Meta sidebar panel to view.
 -->
あなたのバインドされたブロックはすべて、そのコンテンツを投稿メタフィールドに保存するので、将来、あなたのデータの整合性を失うことなく、コンテンツモデルを再デザイン、リミックス、フィルタリングできます。表示するには、「投稿メタ」サイドバー・パネルを開いてください。

<!-- 
![data-model-post-meta](https://github.com/user-attachments/assets/7232d9b7-8ac3-4159-ba4a-6e94d37ada58)
 -->
![data-model-post-meta](https://github.com/user-attachments/assets/7232d9b7-8ac3-4159-ba4a-6e94d37ada58)

<!-- 
Click the Manage Post Meta button to browse all of your block bindings and create your own custom fields that are available in the post editing screen.
 -->
Manage Post Meta ボタンをクリックして、すべてのブロック・バインディングをブラウズし、投稿編集画面で利用可能な独自のカスタムフィールドを作成します。

<!-- 
![data-model-post-meta-custom-fields](https://github.com/user-attachments/assets/f7ee2af7-1753-41ec-885d-4cf9b3669a93)
 -->
![data-model-post-meta-custom-fields](https://github.com/user-attachments/assets/f7ee2af7-1753-41ec-885d-4cf9b3669a93)

<!-- 
Click **Publish** to see your new content model on your website.
 -->
**Publish** をクリックすると、Web サイトにあなたの新規コンテンツモデルが表示されます。

<!-- 
## Adding and managing content
 -->
## コンテンツの追加と管理

<!-- 
Once your data model is published, it will show up as an additional post type beneath Posts and Pages in your WordPress dashboard. 
 -->
あなたのデータモデルが公開されると、あなたの WordPress ダッシュボードの「投稿」と「ページ」の下に、追加の投稿タイプとして表示されます。

<!-- 
Add new content just like you would add any other post content. You’ll notice that only the blocks you bound are editable, and the rest of the data model’s template is safe from being changed or edited.
 -->
他の投稿コンテンツを追加するのと同じように、新規コンテンツを追加します。あなたがバインドしたブロックだけが編集可能で、データモデルのテンプレートの残りの部分は変更や編集から保護されていることに気づくでしょう。

<!-- 
![data-model-content-group](https://github.com/user-attachments/assets/eac3b513-175b-480b-9777-94fa6cc340b1)
 -->
![data-model-content-group](https://github.com/user-attachments/assets/eac3b513-175b-480b-9777-94fa6cc340b1)

<!-- 
Any custom fields that you’ve added will also be available in the post sidebar:
 -->
あなたが追加したカスタムフィールドは、投稿サイドバーでも利用できるようになります:

<!-- 
![data-model-custom-fields](https://github.com/user-attachments/assets/39b485a1-cf3a-492a-a497-969d1ca14040)
 -->
![data-model-custom-fields](https://github.com/user-attachments/assets/39b485a1-cf3a-492a-a497-969d1ca14040)

<!-- 
Click the **Publish** button to publish your post and view it on the front end. 
 -->
**Publish** ボタンをクリックすると、あなたの投稿が公開され、フロントエンドに表示されます。

<!-- 
## Updating the front-end layout
 -->
## フロントエンド・レイアウトの更新

<!-- 
Create Content Model is designed to work with the block editor and block-based themes. If you’d like to make changes to the design of the single or archive templates for your custom post type, you can do that inside of the Site Editor, just like you would for any other post type. 
 -->
Create Content Model は、ブロックエディタとブロックベースのテーマで動作するように設計されています。カスタム投稿タイプの個別テンプレートやアーカイブテンプレートのデザインを変更したい場合は、他の投稿タイプと同じようにサイトエディタ内で変更できます。

<!-- 
### Single post template
 -->
### 個別投稿テンプレート

<!-- 
You can set up the single post layout in your custom post type template. Alternatively, you can create a new `single-CPTNAME.html` template and add block variations from the block inserter.
 -->
あなたのカスタム投稿タイプ・テンプレートで、個別投稿レイアウトを設定できます。あるいは、新規 `single-CPTNAME.html` テンプレートを作成し、ブロック・インサーターからブロック・バリエーションを追加できます。

<!-- 
### Archives and the Query Loop block
 -->
### アーカイブと Query Loop ブロック

<!-- 
Create a custom [Query Loop](https://wordpress.org/documentation/article/query-loop-block/) on a page, `archive-CPTNAME.html` template, or any other template (e.g. the theme’s home template). Pull in the posts from your data model, sort and filter them, and use the new block variations in the block inserter to pull individual pieces of data into your template.
 -->
ページ、`archive-CPTNAME.html` テンプレート、またはその他のテンプレート (テーマのホームテンプレート、など) にカスタム [Query Loop](https://wordpress.org/documentation/article/query-loop-block/) を作成します。あなたのデータモデルから投稿を取り込み、ソートとフィルタリングを行い、ブロック・インサータの新規ブロック・バリエーションを使って、個々のデータをあなたのテンプレートに取り込みます。

<!-- 
![data-model-query-loop](https://github.com/user-attachments/assets/a5023781-4ce8-426f-9e9d-46eb7ce35795)
 -->
![data-model-query-loop](https://github.com/user-attachments/assets/a5023781-4ce8-426f-9e9d-46eb7ce35795)

<!-- 
## Plugin export workflow
 -->
## プラグイン・エクスポートのワークフロー

<!-- 
Create Content Model is a development tool, but it’s not required to run on your site. If you’re done building your content model, you can “export” it as a standalone plugin:
 -->
Create Content Model は開発ツールですが、あなたのサイトで実行する必要はありません。あなたのコンテンツモデルを構築し終えたら、スタンドアローンのプラグインとして「エクスポート」できます:

<!-- 
1. Click Content Models → **Export**.
2. Export the data model plugin by clicking the **Download ZIP fil**e button.
3. Install your data model plugin on a new site (or deactivate the main plugin on the current site and import the new plugin). Remember to upload it as the .zip file.
4. Optionally, add version control for your own content model plugin to track changes and deploy your plugin across multiple sites.
 -->
1. コンテンツモデルをクリック → **Export** します。
2. **Download ZIP file** ボタンをクリックして、データモデル・プラグインをエクスポートします。
3. 新規サイトにあなたのデータモデル・プラグインをインストールします (または現在のサイトのメインプラグインを無効にして、新規プラグインをインポートします)。.zip ファイルとしてアップロードすることを忘れないでください。
4. 必要に応じて、独自のコンテンツモデル・プラグインにバージョン管理を追加して、変更を追跡し、複数のサイトにわたってあなたのプラグインを展開します。

<!-- 
## Test locally with Studio
 -->
## Studio でローカル・テスト

<!-- 
Studio is WordPress.com's free, open-source local development environment.
 -->
Studio は、WordPress.com 製の、無償で利用できるオープンソースのローカル開発環境です。

<!-- 
1. Download [Studio](https://developer.wordpress.com/studio/?utm_source=github&utm_medium=get-started&utm_campaign=create-content-model).
2. Add a site.
3. Open WP Admin.
4. Download the [latest plugin release](https://github.com/Automattic/create-content-model/releases/latest/download/create-content-model.zip).
5. Install and activate the plugin.
 -->
1. [Studio](https://developer.wordpress.com/studio/?utm_source=github&utm_medium=get-started&utm_campaign=create-content-model) をダウンロードします。
2. サイトを追加します。
3. WordPress 管理画面を開きます。
4. [Create Content Model プラグインの最新リリース](https://github.com/Automattic/create-content-model/releases/latest/download/create-content-model.zip)をダウンロードします。
5. プラグインをインストールし、有効化します。