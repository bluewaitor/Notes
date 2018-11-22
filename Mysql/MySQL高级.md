# MySQL高级

## trigger触发器

insert/update/delete 可以触发 insert/upadte/delete

监视谁
监视动作
触发时间
触发事件

create trigger triggername
before/after
insert/update/delete
on tablename
for each row
begin
declare rnum int;

insert/update/delete new.fieldname/old.fieldname
end;
