#### 快捷键

```
-Xms1024M -Xmx1024M -XX:PermSize=512M -XX:MaxPermSize=512M
```

```java
/**
 * 快捷键
 * @author xuxh ctrl +shift+l查询快捷键
 * 1:ctrl+shift+t 源码 ctrl+t接口实现类
 * 2:ctrl+shift+r打开资源
 * 3:ctrl+shift+g 查找引用此类或方法的地方
 * 3:ctrl+o 类概要
 * 4:ctrl+t 类继承关系
 * 4:ctrl+shift+l 两次显示key
 * 5:ctrl+alt+h类被哪些调用
 * 6:ctrl+shift+left/right 单词选中
 * 7:ctrl+m 窗口最大最小化
 * 8:ctrl+PgDn/PgUp 窗口切换
 * 9:alt+↑/↓ 选中一行
 * 10：ctrl+L 查询行
 * 11：ctrl+shift+X 变大写
 * 12：ctrl+shift+Y 变小写
 * 13: ctrl+o 查看类中方法和属性
 * 14：ctrl+h查找
 */
public class KeyHot {
       // alt +shift+r为属性方法重命名
       private String nickname ;
       // alt +shift+g搜索引用
       public String getName() {
             return nickname ;
      }
       public static void main(String[] args) {
            Calendar calendar = Calendar. getInstance();
             // ctrl +2本地变量赋值
             // alt +shift+r重命名
            calendar.add(1, 2);
             // shift+enter之下创建一个空白行， ctrl+shift+enter下面
            System. out.println("xuxiaohui" );
             // alt +方向键上下移
            System. out.println("yangguang" );
      }
       public void print() {
             // ctrl +.移动到下一个错误
            File file = new File( "");
             // ctrl +1解决问题
      }
}
```

