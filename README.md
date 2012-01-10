# ssh-plugin
## 概要
jenkinsでssh-pluginを利用していますが、ビルドパラメータや[環境変数](https://wiki.jenkins-ci.org/display/JA/Building+a+software+project#Buildingasoftwareproject-Jenkins%E3%81%8C%E8%A8%AD%E5%AE%9A%E3%81%99%E3%82%8B%E7%92%B0%E5%A2%83%E5%A4%89%E6%95%B0)が使えないので使えるように試作してみました。

## ビルドパラメータ、環境変数の使い方
ビルドパラメータはそのままの名前で使用できます。

環境変数はJENKINS_を頭に付けると使用できます。

    echo $hoge
    echo $JENKINS_HOME

## その他
実装としてはシェルで最初に以下を実行しているだけです。

    [key]="[value]"; export [key];

