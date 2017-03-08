# mybatis-
mybatis升级到3.2以上版本对应association标签的使用需要修改
低版本支持以下这种写法，查询结果数量与实际结果一致
<resultMap ...>
   <association .../>
   <association .../>
</resultMap>
3.2以上版本的写法必须增加唯一属性
<resultMap ...>
   <result property="id"    column="id" />
   <association .../>
   <association .../>
</resultMap>
否则会出现查询结果的数量缺少。
