# AnimationTest
#1 Unity5のAnimationの検証用です<br />
1. animationTestのSceneを開く<br />
2. Baseの階層を見る<br />
3. Sphere_BaseにAnimatorが有ります。<br />
　New Animator Controllerの中に<br />
　moveとmove2の二つのAnimが配置してあります。<br />
　<br />
　moveの方のアニメをAnimationウィンドウで確認すると、Sphere_Baseを含めたアニメが確認できます。<br />
　Sceneを再生してみましょう。<br />
　Animationウィンドウで確認したのとはことなる動作をします。<br />
　<br />
　合わせる為には、AnimatorのApplyRootMotionのチェックを外す必要があります。<br />
　このプロジェクトをUnity4系で開いてみると、ApplyRootMotionのチェックを外さなくてもAnimationウィンドウと
　同じアニメが再生されます。<br />
　<br />
#1 解説<br />
Animationのチュートリアルに個々の説明が書かれています。<br />
https://www.youtube.com/watch?v=Kn6jxLWA31M<br />
<br />
Unity4とUnity5ではApplyRootMotionの意味合いが変わりました。<br />
4では、絶対座標としてAnimationを扱い「ApplyRootMotion」することでRootMotionの座標にSetしています。<br />
5では「ApplyRootMotion」することでMotionの初期値を相対的に扱う事が出来るようになっています。<br />
<br />
#1 注意点<br />
チュートリアルの動画にあるような、「GenerateRootMotionCurves」のボタンはUnityで作成したAnimationにしか表示されません。<br />
3Dモデルにモーションをつけ、FBXなどで持ってきた場合、動画の場所ではなく、FBXImport Settings のAnimationsの中で
モーションを切り出した際、Motionの項目でRootMotionNodeでDedaultNodeを設定できます。<br />
ここでNodeを設定すると、「GenerateRootMotionCurves」を押したのと同じ事になるみたいです。<br />
