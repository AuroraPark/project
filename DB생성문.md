# 0. db생성문

```

```


# 1. 시퀀스 생성문
```
create sequence seq_mf_code
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
create sequence seq_mml_reply_code
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
create sequence seq_qna_no
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
create sequence seq_mml_num
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
create sequence seq_bs_bno
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
create sequence seq_bf_bno
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
create sequence seq_bs_rno
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
create sequence seq_bfr_rno
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
```

# 2. (필요시) 시퀀스 삭제문

```
DROP SEQUENCE seq_mf_code;
DROP SEQUENCE seq_mml_reply_code;
DROP SEQUENCE seq_qna_no;
DROP SEQUENCE seq_mml_num;
DROP SEQUENCE seq_bs_bno;
DROP SEQUENCE seq_bf_bno;
DROP SEQUENCE seq_bs_rno;
DROP SEQUENCE seq_bfr_rno;
```

# 3. MML_CONTENT 테이블 수정사항입니다.
1. mi_code : number -> varchar2(100)
2. mi_code에 여러개의 영화코드가 들어감(ex: 3,5,1,4)
3. mml_poster에 여러개의 영화포스터 파일명이 들어감(ex:test.jpg,test1.jpg,test2.jpg) -> 첫번째 파일명을 추출해서 썸네일로 사용하면 됨

```
ALTER TABLE mml_content DROP CONSTRAINT fk_movie_info_to_mml_content;
ALTER TABLE MML_CONTENT MODIFY (MI_CODE VARCHAR2(100) );
```

# 4. board_free 수정
```
ALTER TABLE board_free DROP COLUMN bf_thumb;
ALTER TABLE board_free ADD(bf_recommend NUMBER);
ALTER TABLE board_free ADD(bf_decommend NUMBER);
```

# 5. 트리거(board_qna삭제시 admin_qna삭제)
```
create or replace trigger boardQna_to_adQna_delete
before delete on BOARD_QNA for each row
begin
delete AD_QNA where qna_no = :old.qna_no;
end;
/
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDU4MjQ3OTAxXX0=
-->