langchain-streamlit-app
このリポジトリは、Streamlit + LangChain + OpenAI（ChatOpenAI）を使って簡単なチャットアプリを作るサンプルだよ。
ChatGPT API の一部機能を活用して、ユーザーの入力を受け取り、会話形式でレスポンスを返す仕組みになってるよ。

1. 概要
Streamlit を使って手軽にウェブアプリのUIを構築
LangChain と OpenAI API の連携でチャット機能を実装
環境変数から モデル名 や temperature を取得して柔軟に設定可能
2. 必要な環境とインストール
必要なもの
Python 3.8 以上（3.10あたりが無難かも）
pip などのパッケージマネージャー
OpenAIのAPIキー（OpenAI公式サイトで取得可能）
.env ファイルで環境変数を設定
インストール手順
bash
コピーする
編集する
# リポジトリをクローン or ダウンロードして、そのディレクトリへ移動
git clone https://github.com/your-repo/langchain-streamlit-app.git
cd langchain-streamlit-app

# 必要なPythonパッケージをインストール
pip install -r requirements.txt

# または単体で
pip install streamlit
pip install python-dotenv
pip install openai
pip install langchain
3. 環境変数の設定
リポジトリのルートに .env ファイルを用意して、以下の変数を設定してね。

txt
コピーする
編集する
OPENAI_API_KEY=sk-xxxxxxx       # あなたのOpenAI APIキー
OPENAI_API_MODEL=gpt-3.5-turbo  # 好みのモデル
OPENAI_API_TEMPERATURE=0.7      # 好みの温度パラメータ
OPENAI_API_KEY: OpenAIのAPIキー
OPENAI_API_MODEL: 使用するモデル（gpt-3.5-turbo や gpt-4 など）
OPENAI_API_TEMPERATURE: モデルの出力の創造性を調節する値（0～1の範囲が多め）
4. 使い方
.env を正しく設定したら、以下のコマンドでアプリを起動
bash
コピーする
編集する
streamlit run app.py
ブラウザが自動的に立ち上がり、localhost:8501 などでアプリが表示されるよ。
テキストボックスに入力して「Enter」すると、アシスタントが返信してくれるよ。
