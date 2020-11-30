# Ark_birthdays_search_demo
  <h1 align="left">
    明日方舟干员生日查询
    <br/>
  </h1>
  一个基于python中urllib库爬取网页信息的简易项目。爬取的网页是明日方舟Wiki，即prts中干员们的生日信息。目前内核没有使用scrapy框架，只是一个非常简单的练习。后续使用了框架开发会尝试加上GUI。  
  
  使用前需要安装python环境，推荐安装python3.7以上版本。
  
  说明：trial.zip中包含了四个文件，其中trial.py负责爬取prts中明日方舟干员的名字及生日信息，并使用pickle将列表保存到本地中以便重复查询而不必反复爬取prts获得信息。birth_easydemo.py则打开birthdays.pik和operators.pik获得生日列表和干员名列表，并面向用户提供查询功能。理论上即使prts更新了新的干员的信息，只要再次运行trial.py就可以更新birthdays.pik和operators.pik的内容，从而在birth_easydemo.py中可以查询到更新后的干员的生日。
  
  由于prts上如果想要通过“点击干员名”的链接就直接访问对应干员页面的过程中遇到了python的scrapy无法渲染js的问题，而这个问题以我的水平又暂时无法解决。故权且采用较笨的方法，直接使用urllib库访问干员档案页面中查找干员生日信息，这种办法在全干员资料都在prts档案页面上的情况下或许是最优解，但是经过浏览页面可知，档案页面上并没有一星干员Lancet-2、Castle-3、THRM-EX的生日（出厂日）资料，需要自行手动添加，这样就较为麻烦。而且干员生日资料中存在部分干员生日“未知”、“本人表示遗忘”等情况，也要将干员列表operators_list中剔除无生日资料的干员名，显得尤为笨重。  
  
  再者，本demo使用的查询方法是通过Index查询，可能存在干员对应生日的问题，虽然经过多次测试未发现此问题，但终究不太放心，将在后续（如果不咕）的更新中使用新的方法。  
