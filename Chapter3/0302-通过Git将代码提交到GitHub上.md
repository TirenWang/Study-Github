* 1 前言
  在「利用 SSH 完成 Git 与 GitHub 的绑定」一文中，我们完成了本地 Git 与远程 GitHub 的绑定，这意味着我们已经可以通过 Git 向 GitHub 提交代码啦！但是在进行演示之前，我们需要先了解两个命令，也是我们在将来需要经常用到的两个命令，分别为push和pull.

  push：该单词直译过来就是“推”的意思，如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库，代码示例：
  git push origin master
  1
  pull：该单词直译过来就是“拉”的意思，如果我们远程仓库的代码有了更新，同样为了保持本地与远程的代码同步，我们就需要把远程的代码拉到本地，代码示例：
  git pull origin master
  1
  此外，在之前我们讲到过pull request，在这里，估计大家就能更好的理解了，它表示：如果我们fork了别人的项目（或者说代码），并对其进行了修改，想要把我们的代码合并到原始项目（或者说原始代码）中，我们就需要提交一个pull request，让原作者把我们的代码拉到 ta 的项目中，至少对于 ta 来说，我们都是属于远程端的。

  一般情况下，我们在push操作之前都会先进行pull操作，这样不容易造成冲突。

  2 提交代码
  对于向远处仓库（GitHub）提交代码，我们可以细分为两种情况：

  第一种：本地没有 Git 仓库，这时我们就可以直接将远程仓库clone到本地。通过clone命令创建的本地仓库，其本身就是一个 Git 仓库了，不用我们再进行init初始化操作啦，而且自动关联远程仓库。我们只需要在这个仓库进行修改或者添加等操作，然后commit即可。
  接下来，以博主的 GitHub 账号中的mybatis-tutorial项目为例，进行演示。首先，进入 GitHub 个人主页：

  

  如上图所示，点击mybatis-tutorial项目：

  

  如上图所示，进入mybatis-tutorial项目后，点击Clone or download，复制上图所示的地址链接。然后，进入我们准备存储 Git 仓库的目录，例如下面我们新建的GitRepo目录， 从此目录进入 Git Bash：

  

  接下来，输入git clone https://github.com/guobinhit/mybatis-tutorial.git命令，其中clone后面所接的链接为我们刚刚复制的远程仓库的地址：

  

  如上图所示，我们已经把远程的mybatis-tutorial仓库clone到本地啦！下面，我们看看clone到本地的仓库内容与远程仓库的内容，是否完全一致：

  

  如上图所示，显示我们已经把远程仓库mybatis-tutorial的内容都clone到本地啦！接下来，为了方便演示，我们直接把之前重构的「史上最简单的 MyBatis 教程」里面的mybatis-demo项目的代码复制过来：

  

  如上图所示，我们已经把mybatis-demo项目里面的主要内容src目录和web目录复制过来啦！接下来，从此目录进入 Git Bash，然后输入git status命令查看仓库状态：

  

  如上图所示，mybatis-tutorial已经是一个 Git 仓库了，而且在输入git status命令后显示有两个文件未被追踪，也就是我们刚刚复制过来的两个文件没有提交。通过「Git 初体验及其常用命令介绍」，我们已经知道了在真正提交代码之前，需要先进行git add操作：

  

  如上图所示，我们已经将src目录add并commit到mybatis-tutorial仓库啦！接下来，我们将web目录提交到仓库，然后输入git log命令查看仓库日志：

  

  再输入git status命令查看仓库状态：

  

  如上图所示，我们已经将mybatis-tutorial仓库里面新添加的两个目录都提交啦！下面，我们将本地仓库的内容push到远程仓库，输入git push origin master命令：

  

  如上图所示，在第一次向远程仓库提交代码的时候，需要输入账号及密码进行验证，验证成功后，显示如下结果：

  

  然后，刷新 GitHub 中mybatis-tutorial仓库：

  

  如上图所示，我们已经将项目（仓库）中新添加的内容提交到了远程仓库。接下来，返回 GitHub 个人主页：

  

  观察上图，我们会发现一个现象，那就是：mybatis-tutorial仓库的概要中新增了一个Java语言的标记。对于这个仓库语言的标记，其来源有两个，一是在我们创建仓库时就指定语言；二是在我们提交或者新建代码后由 GitHub 自动识别该语言。

  第二种：详见「通过 Git 将代码提交到 GitHub（下）」.

  最后，附上博主的 GitHub 账号，欢迎大家 Follow：：[Tiren Wang](https://github.com/TirenWang)

  ------------------------------------------------

  