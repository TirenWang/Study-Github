* 在「通过 Git 将代码提交到 GitHub（上）」一文中，我们已经介绍了向 GitHub 提交代码时的第一种情况，即：

  第一种：本地没有 Git 仓库，这时我们可以直接将远程仓库clone到本地。通过clone命令创建的本地仓库，其本身就是一个 Git 仓库了，不用我们再进行init初始化操作啦，而且自动关联远程仓库。我们只需要在这个仓库进行修改或者添加等操作，然后commit即可。
  接下来，我们继续介绍向 GitHub 提交代码时可能遇到的第二种情况，即：

  第二种：本地有 Git 仓库，并且我们已经进行了多次commit操作。
  仍然以博主的开源项目为例，不过这次换成springmvc-tutorial项目进行演示。首先，建立一个本地仓库，命名为springmvc-tutorial：

  

  如上图所示，进入该仓库，进入init初始化操作：

  

  然后，输入git remote add origin https://github.com/guobinhit/springmvc-tutorial.git命令，关联远程仓库（在此，默认大家都知道如何获取远程仓库的地址），其中origin为远程仓库的名字：

  

  输入git pull origin master命令，同步远程仓库和本地仓库：

  

  再回到本地springmvc-tutorial仓库，看看我们是否已经把远程仓库的内容同步到了本地：

  

  如上图所示，显然我们已经把远程springmvc-tutorial仓库里面仅有的README.md文件同步到了本地仓库。接下来，在本地仓库新建一个名为test.txt的测试文件：

  

  输入git add和git commit命令，将文件test.txt添加并提交到springmvc-tutorial仓库：

  

  再输入git push origin master命令，将本地仓库修改（或者添加）的内容提交到远程仓库：

  

  如上图所示，我们已经将本地仓库的内容同步到了远程仓库。下面，我们进入远程springmvc-tutorial仓库的页面，看看我们的提交结果：

  

  如上图所示，我们已经将「通过 Git 将代码提交到 GitHub」的第二种情况演示完毕。

  此外，在本篇博文中，我们将远程仓库命名为origin，本地仓库名为springmvc-tutorial，其实两者的名字咱们可以随意取，一般来说，我们习惯性将远程仓库命名为origin，不过在需要关联多个远程仓库的时候，就需要我们再取别的名字啦！

  最后，再强调一遍：在我们向远程仓库提交代码的时候，一定要先进行pull操作，再进行push操作，防止本地仓库与远程仓库不同步导致冲突的问题，尤其是第二种提交代码的情况，很容易就出现问题。

  

  最后，附上博主的 GitHub 账号，欢迎大家 Follow：：[Tiren Wang](https://github.com/TirenWang)

  ------------------------------------------------

  