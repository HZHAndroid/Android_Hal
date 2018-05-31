### tar命令(https://www.cnblogs.com/yhjoker/p/7568680.html)
    压缩： 
    tar -cvjPf etc.tar.bz2 /etc　　//-c为创建一个打包文件，相应的-f后面接创建的文件的名称，使用了.tar.bz2后缀，-j标志使用bzip2压缩，最后面为具体的操作对象/etc目录

    查看：
       tar -tvjf　etc.tar.bz2　　　　　//-t为查看操作，则-f对应所查看的文件的名称，文件后缀显示使用bzip2进行压缩，所以加入-j选项，-v会显示详细的权限信息

    解压
       tar -xvjf　etc.tar.bz2　　　　　//-x为解压操作，则-f指定的是解压使用的文件，文件后缀显示使用bzip2进行压缩，所以加入-j选项，即使用bzip2解压
                         //若只解压指定打包文件中的一个文件，在上述指令的最后加上带解压文件名作为参数即可
