# AnimationTest
#1 Unity5のAnimationの検証用プロジェクトです。
1. animationTestのSceneを開く
2. Baseの階層を見る
3. Sphere_BaseにAnimatorが有ります。
　New Animator Controllerの中に
　moveとmove2の二つのAnimが配置してあります。
　
　moveの方のアニメをAnimationウィンドウで確認すると、Sphere_Baseを含めたアニメが確認できます。
　Sceneを再生してみましょう。
　Animationウィンドウで確認したのとはことなる動作をします。
　
　合わせる為には、AnimatorのApplyRootMotionのチェックを外す必要があります。
　このプロジェクトをUnity4系で開いてみると、ApplyRootMotionのチェックを外さなくてもAnimationウィンドウと
　同じアニメが再生されます。
　
