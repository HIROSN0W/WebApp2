# WebApp2
<div style="text-align: right;">
3I24 中川寛之
</div>

## 目的

- Javascript/Typescriptを使ってみる
- フロントエンドフレームワークReactを使ってみる
- Webアプリケーション開発における、フロントエンド開発、バックエンド開発、デザイン開発の関係性を理解する
- Git/GitHubを使った開発を行う

## 使用したツール

- docker
- Node.js
- React 

## 環境構築1: 
作成したシステムの概略
- Reactの開発環境の設備
- Typescript,SWC,Viteの活用
- hot reloadの有効化
- ベースになるReactアプリケーションの作成

動作確認の方法と結果
![alt text](image.png)


## 課題1-1: 適当な文字列を表示するようにReactアプリケーションの作成

動作確認の方法と結果

<関数>
```tsx
const Sample2:React.FC<{prop:String}> = ({prop}) => {
  return (
    <div key="Sample2">
      <p>{prop}</p>
    </div>
  )

}
```
```tsx
const Sample3:React.FC <{prop:{name:String, message:String}}> = ({prop}) =>{
  return (
    <div key="Sample3">
      <br>{prop.name}</br>
      <p>{prop.message}</p>
    </div>
  )
}
```
<入力値>
```tsx
function App() {
  return (
    <div className="App">
      <header className="App-header">
        <Sample></Sample>
        <Sample2 prop="3I24 中川" ></Sample2>
        <Sample3 prop={{name:"寛之",message:"300円でトルネードポテト売ってます"}}></Sample3>
      </header>
    </div>
  );
}
```
<結果>
![alt text](image-1.png)


## 課題1-2: Clockコンポーネントの実装
動作確認の方法と結果

<Clockコンポーネント>

```tsx
const Clock: React.FC = () => {
  const [state, setState] = useState<Date>(new Date())

  useEffect(() => {
    setInterval(
      () => { setState(new Date()) }
      , 1000);
  }, []);

  return (
    <div key="clock">
      <p>{state.toString()}</p>
    </div>
  )
}
```
![alt text](image-3.png)


## 課題2: 掲示板アプリの作成
作成したシステムの概略  

- Appコンポーネント
- PostedMessagesコンポーネント
- PostedMessageコンポーネント
- CommentFormコンポーネント
の作成

動作確認の方法と結果

<掲示板アプリの流れ>
ユーザーがCommentForm内の名前とメッセージ内容を入力し、submitボタンを押すと、AppコンポーネントのaddMessage()が呼び出され、新規メッセージがmessages配列に追加される。
messagesが更新されるたびにPostedMessagesコンポーネントが再びレンダリングされ、最新のメッセージ一覧がリアルタイムにブラウザに表示される。
そのため、Submitボタンを押して、リアルタイムでWebページに追加させたことが確認されればよい。

<画像>
![alt text](image-5.png)



## 選択課題: 
作成したシステムの概略
動作確認の方法と結果
## 理解したこと、理解できていないこと






## 写真フォルダー



![alt text](image-4.png)
