### tar命令(https://www.cnblogs.com/yhjoker/p/7568680.html)
    压缩： 
    tar -cvjPf etc.tar.bz2 /etc　　//-c为创建一个打包文件，相应的-f后面接创建的文件的名称，使用了.tar.bz2后缀，-j标志使用bzip2压缩，最后面为具体的操作对象/etc目录

    查看：
       tar -tvjf　etc.tar.bz2　　　　　//-t为查看操作，则-f对应所查看的文件的名称，文件后缀显示使用bzip2进行压缩，所以加入-j选项，-v会显示详细的权限信息

    解压
       tar -xvjf　etc.tar.bz2　　　　　//-x为解压操作，则-f指定的是解压使用的文件，文件后缀显示使用bzip2进行压缩，所以加入-j选项，即使用bzip2解压
                         //若只解压指定打包文件中的一个文件，在上述指令的最后加上带解压文件名作为参数即可

### linux把文件压缩成.tar.gz的命令
    01-.tar格式
    解包：[＊＊＊＊＊＊＊]$ tar xvf FileName.tar
    打包：[＊＊＊＊＊＊＊]$ tar cvf FileName.tar DirName（注：tar是打包，不是压缩！）
    02-.gz格式
    解压1：[＊＊＊＊＊＊＊]$ gunzip FileName.gz
    解压2：[＊＊＊＊＊＊＊]$ gzip -d FileName.gz
    压 缩：[＊＊＊＊＊＊＊]$ gzip FileName

    03-.tar.gz格式
    解压：[＊＊＊＊＊＊＊]$ tar zxvf FileName.tar.gz [-C 输出路径]
    压缩：[＊＊＊＊＊＊＊]$ tar zcvf FileName.tar.gz DirName

    04-.bz2格式
    解压1：[＊＊＊＊＊＊＊]$ bzip2 -d FileName.bz2
    解压2：[＊＊＊＊＊＊＊]$ bunzip2 FileName.bz2
    压 缩： [＊＊＊＊＊＊＊]$ bzip2 -z FileName

    05-.tar.bz2格式
    解压：[＊＊＊＊＊＊＊]$ tar jxvf FileName.tar.bz2
    压缩：[＊＊＊＊＊＊＊]$ tar jcvf FileName.tar.bz2 DirName

    06-.bz格式
    解压1：[＊＊＊＊＊＊＊]$ bzip2 -d FileName.bz
    解压2：[＊＊＊＊＊＊＊]$ bunzip2 FileName.bz

    07-.tar.bz格式
    解压：[＊＊＊＊＊＊＊]$ tar jxvf FileName.tar.bz

    08-.Z格式
    解压：[＊＊＊＊＊＊＊]$ uncompress FileName.Z
    压缩：[＊＊＊＊＊＊＊]$ compress FileName

    09-.tar.Z格式
    解压：[＊＊＊＊＊＊＊]$ tar Zxvf FileName.tar.Z
    压缩：[＊＊＊＊＊＊＊]$ tar Zcvf FileName.tar.Z DirName

    10-.tgz格式
    解压：[＊＊＊＊＊＊＊]$ tar zxvf FileName.tgz

    11-.tar.tgz格式
    解压：[＊＊＊＊＊＊＊]$ tar zxvf FileName.tar.tgz
    压缩：[＊＊＊＊＊＊＊]$ tar zcvf FileName.tar.tgz FileName

    12-.zip格式
    解压：[＊＊＊＊＊＊＊]$ unzip FileName.zip
    压缩：[＊＊＊＊＊＊＊]$ zip FileName.zip DirName

    13-.lha格式
    解压：[＊＊＊＊＊＊＊]$ lha -e FileName.lha
    压缩：[＊＊＊＊＊＊＊]$ lha -a FileName.lha FileName

    14-.rar格式
    解压：[＊＊＊＊＊＊＊]$ rar a FileName.rar
    压缩：[＊＊＊＊＊＊＊]$ rar e FileName.rar      
    rar请到：下载！
    解压后请将rar_static拷贝到/usr/bin目录（其他由$PATH环境变量
    指定的目录也行）：[＊＊＊＊＊＊＊]$ cp rar_static /usr/bin/rar
