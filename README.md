Printtable是一个可以在terminal上输出数据表样式的python包。

 ![image](https://raw.githubusercontent.com/Leviathan1995/Pylsy/master/pzi/span.png)
 

<h2>下载方式</h2>
       pip install printtable

<h2>使用示例</h2>
<h6>引用printtable</h6>
       from  printtable import PrintTable
<h6>首先我们需要构建表的表头，然后创建表</h6>
       attributes=[['name','old']]
       table = PrintTable(attributes)
<h6>然后我们有两种方式向表内加入数据</h6>

 1. `append_data`:可以通过明确特征来加入一行数据中的一部分数据或者多行数据。
    
        table.append_data(name="Jack",old = "20")
        table.append_data(name =["Jack","Mary"], old =["20","19"])
 2. `append_data_list`: 可以直接使用list格式的变量向表中加入一行数据。不过要注意数据的顺序要符合创建表时的表头相同。
 
        table.append_data_list(["Jack","20"]) 

<h6>最后我们可以在terminal直接输出ASCII表。通过line_num参数来控制在每行数据前是否加上行号，１为加入，默认为不加入行号。</h6>
       table.printTable(1)
       table.printTable()
