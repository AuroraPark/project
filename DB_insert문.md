> /* 멤버 추가 */

insert into member
		values (seq_member_id.nextval, '닉넴넴', null, 'test@test.com', 'Y', 'Y', '현민현밓','010-1234-1234', 'Y', '1234',
				sysdate, sysdate, 'N', 0, 0, 0, 1, 'Y');
                
                
                
> /* 자게 게시글 추가 */

INSERT INTO board_free VALUES (seq_bf_bno.nextval, 2, 0, 0, '카테고리머지', 
		'자유게시판게시글제목!!', sysdate, sysdate, '출처!!!!', '게시판 내용 뭐넣지!!!!',
		0, 0, 'N');
        
> /* 공유 게시글 추가 */

INSERT INTO board_share VALUES (seq_bs_bno.nextval, 2, '카테고리머지',
	'공유합니당!!!내용이에요!!!!', '공유합니다!!제목이에요', sysdate, sysdate,
	0, 0, 'N');

> /* 나영리 게시글 추가 */

insert into mml_content values (seq_mml_num.nextval, 1, 2, 0, sysdate, sysdate, 
		0, '떠나자!', '안녕핫에요 나영리 컨텐츠에요', '사진링크', 0);

> /* 공지사항 추가 */

INSERT INTO ad_notice VALUES (seq_ad_notice_no.nextval, 1, '공지 내용 뭐넣지!!!!'
    ,'공지사항 제목!!', sysdate, sysdate );

> /* 1:1 문의 등록 */

insert into board_qna values (seq_qna_no.nextval, 2, '문의', '문의제목드립니다.'
		, '문의내용입니다!!!!!!!!!!!!!!!!!!!!11!', sysdate, sysdate, 'N');
    
> /* 1:1 답변 등록 */

insert into ad_qna values (seq_ad_qna_no.nextval, 1, '답변내용입니다!!!!!', sysdate, sysdate, 2);


    > /* 멤버 추가 */

insert into member
		values (seq_member_id.nextval, '닉넴넴', null, 'test@test.com', 'Y', 'Y', '현민현밓','010-1234-1234', 'Y', '1234',
				sysdate, sysdate, 'N', 0, 0, 0, 1, 'Y');
                
                
                
> /* 자게 게시글 추가 */

INSERT INTO board_free VALUES (seq_bf_bno.nextval, 3, 0, 0, '카테고리머지', 
		'삼번사용자!!', sysdate, sysdate, '출처!!!!', '게시판 내용 뭐넣지!!!!',
		0, 0, 'N');
        
> /* 공유 게시글 추가 */

INSERT INTO board_share VALUES (seq_bs_bno.nextval, 3, '카테고리머지',
	'삼번사용자!!!내용이에요!!!!', '삼번사용자공유합니다!!제목이에요', sysdate, sysdate,
	0, 0, 'N');

> /* 나영리 게시글 추가 */

insert into mml_content values (seq_mml_num.nextval, 1, 3, 0, sysdate, sysdate, 
		0, '삼번사용자떠나자!', '삼번사용자 나영리 컨텐츠에요', '사진링크', 0);

> /* 공지사항 추가 */

INSERT INTO ad_notice VALUES (seq_ad_notice_no.nextval, 1, '공지 내용 뭐넣지!!!!'
    ,'공지사항 제목!!', sysdate, sysdate );

> /* 1:1 문의 등록 */

insert into board_qna values (seq_qna_no.nextval, 2, '문의', '문의제목드립니다.'
		, '문의내용입니다!!!!!!!!!!!!!!!!!!!!11!', sysdate, sysdate, 'N');
    
> /* 1:1 답변 등록 */

insert into ad_qna values (seq_ad_qna_no.nextval, 1, '답변내용입니다!!!!!', sysdate, sysdate, 2);


select bf_title from board_free where id=3
union all
select bs_title from board_share where id=3
union all
select mml_title from mml_content where id=3;

/* 답변 작성 */
insert into ad_qna values(seq_ad_qna_no.nextval, 42 , '답변입니다', sysdate, sysdate, '1');
insert into ad_qna values(seq_ad_qna_no.nextval, #{qna_no}, #{aqna_content}, sysdate, sysdate, #{admin_num});


/* 답변 작성 후 qna_answer y로변경 */
update board_qna set qna_answer='Y' where qna_no= 42;
update board_qna set qna_answer='Y' where qna_no= #{qna_no}



/* 답변 수정 */
update ad_qna set aqna_content='답변 수정2', aqna_update_date= sysdate where aqna_no=21;
update ad_qna set aqna_content=#{aqna_content}, aqna_update_date= sysdate where aqna_no=#{aqna_content};




<!--stackedit_data:
eyJoaXN0b3J5IjpbLTYxMjY5NjAzMCw0ODk0NDM5MTIsLTE4ND
kwOTE2NzJdfQ==
-->
