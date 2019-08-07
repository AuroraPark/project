
# 0. 사용자 생성 & db생성문

```
create user blockbuster identified by 1234  
default tablespace users  
temporary tablespace temp;grant connect, dba to blockbuster;
```
```
ALTER TABLE board_free
	DROP
		CONSTRAINT FK_member_TO_board_free
		CASCADE;

ALTER TABLE board_free
	DROP
		CONSTRAINT FK_bf_thumb_TO_board_free
		CASCADE;

ALTER TABLE bf_reply
	DROP
		CONSTRAINT FK_member_TO_bf_reply
		CASCADE;

ALTER TABLE bf_reply
	DROP
		CONSTRAINT FK_board_free_TO_bf_reply
		CASCADE;

ALTER TABLE sns_info
	DROP
		CONSTRAINT FK_sns_code_TO_sns_info
		CASCADE;

ALTER TABLE sns_info
	DROP
		CONSTRAINT FK_member_TO_sns_info
		CASCADE;

ALTER TABLE movie_rev
	DROP
		CONSTRAINT FK_member_TO_movie_rev
		CASCADE;

ALTER TABLE movie_rev
	DROP
		CONSTRAINT FK_movie_info_TO_movie_rev
		CASCADE;

ALTER TABLE cine_rev
	DROP
		CONSTRAINT FK_cine_info_TO_cine_rev
		CASCADE;

ALTER TABLE cine_rev
	DROP
		CONSTRAINT cr_thumb
		CASCADE;

ALTER TABLE bf_thumb
	DROP
		CONSTRAINT FK_board_free_TO_bf_thumb
		CASCADE;

ALTER TABLE bf_thumb
	DROP
		CONSTRAINT FK_member_TO_bf_thumb
		CASCADE;

ALTER TABLE br_thumb
	DROP
		CONSTRAINT FK_bf_reply_TO_br_thumb
		CASCADE;

ALTER TABLE br_thumb
	DROP
		CONSTRAINT FK_member_TO_br_thumb
		CASCADE;

ALTER TABLE board_share
	DROP
		CONSTRAINT FK_member_TO_board_share
		CASCADE;

ALTER TABLE delete_member
	DROP
		CONSTRAINT FK_member_TO_delete_member
		CASCADE;

ALTER TABLE free_warning
	DROP
		CONSTRAINT FK_board_free_TO_free_warning
		CASCADE;

ALTER TABLE free_warning
	DROP
		CONSTRAINT FK_member_TO_free_warning
		CASCADE;

ALTER TABLE bs_warning
	DROP
		CONSTRAINT FK_member_TO_bs_warning
		CASCADE;

ALTER TABLE bs_warning
	DROP
		CONSTRAINT FK_board_share_TO_bs_warning
		CASCADE;

ALTER TABLE mr_thumb
	DROP
		CONSTRAINT FK_movie_rev_TO_mr_thumb
		CASCADE;

ALTER TABLE mr_thumb
	DROP
		CONSTRAINT FK_member_TO_mr_thumb
		CASCADE;

ALTER TABLE mr_warning
	DROP
		CONSTRAINT FK_member_TO_mr_warning
		CASCADE;

ALTER TABLE mr_warning
	DROP
		CONSTRAINT FK_movie_rev_TO_mr_warning
		CASCADE;

ALTER TABLE cr_thumb
	DROP
		CONSTRAINT FK_member_TO_cr_thumb
		CASCADE;

ALTER TABLE cr_thumb
	DROP
		CONSTRAINT FK_cine_rev_TO_cr_thumb
		CASCADE;

ALTER TABLE cr_warning
	DROP
		CONSTRAINT FK_member_TO_cr_warning
		CASCADE;

ALTER TABLE cr_warning
	DROP
		CONSTRAINT FK_cine_rev_TO_cr_warning
		CASCADE;

ALTER TABLE mml_content
	DROP
		CONSTRAINT FK_member_TO_mml_content
		CASCADE;

ALTER TABLE mml_content
	DROP
		CONSTRAINT FK_movie_info_TO_mml_content
		CASCADE;

ALTER TABLE mml_reply
	DROP
		CONSTRAINT FK_member_TO_mml_reply
		CASCADE;

ALTER TABLE mml_reply
	DROP
		CONSTRAINT FK_mml_content_TO_mml_reply
		CASCADE;

ALTER TABLE mml_warning
	DROP
		CONSTRAINT FK_mml_content_TO_mml_warning
		CASCADE;

ALTER TABLE mml_warning
	DROP
		CONSTRAINT FK_member_TO_mml_warning
		CASCADE;

ALTER TABLE mmlr_warning
	DROP
		CONSTRAINT FK_mml_reply_TO_mmlr_warning
		CASCADE;

ALTER TABLE mmlr_warning
	DROP
		CONSTRAINT FK_member_TO_mmlr_warning
		CASCADE;

ALTER TABLE member_follow
	DROP
		CONSTRAINT FK_member_TO_member_follow
		CASCADE;

ALTER TABLE member_follow
	DROP
		CONSTRAINT FK_member_TO_member_follow2
		CASCADE;

ALTER TABLE ad_notice
	DROP
		CONSTRAINT FK_ad_member_TO_ad_notice
		CASCADE;

ALTER TABLE bfr_warning
	DROP
		CONSTRAINT FK_member_TO_bfr_warning
		CASCADE;

ALTER TABLE bfr_warning
	DROP
		CONSTRAINT FK_bf_reply_TO_bfr_warning
		CASCADE;

ALTER TABLE bs_reply
	DROP
		CONSTRAINT FK_board_share_TO_bs_reply
		CASCADE;

ALTER TABLE bs_reply
	DROP
		CONSTRAINT FK_member_TO_bs_reply
		CASCADE;

ALTER TABLE sr_warning
	DROP
		CONSTRAINT FK_member_TO_sr_warning
		CASCADE;

ALTER TABLE sr_warning
	DROP
		CONSTRAINT FK_bs_reply_TO_sr_warning
		CASCADE;

ALTER TABLE board_qna
	DROP
		CONSTRAINT FK_member_TO_board_qna
		CASCADE;

ALTER TABLE ad_qna
	DROP
		CONSTRAINT FK_board_qna_TO_ad_qna
		CASCADE;

ALTER TABLE ad_qna
	DROP
		CONSTRAINT FK_ad_member_TO_ad_qna
		CASCADE;

ALTER TABLE mmlr_thumb
	DROP
		CONSTRAINT FK_member_TO_mmlr_thumb
		CASCADE;

ALTER TABLE mmlr_thumb
	DROP
		CONSTRAINT FK_mml_reply_TO_mmlr_thumb
		CASCADE;

ALTER TABLE blacklist
	DROP
		CONSTRAINT FK_member_TO_blacklist
		CASCADE;

ALTER TABLE board_free
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE bf_reply
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE member
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE sns_info
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE movie_info
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE movie_rev
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE cine_info
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE cine_rev
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE bf_thumb
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE sns_code
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE br_thumb
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE board_share
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE ad_member
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE delete_member
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE mr_thumb
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE cr_thumb
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE cr_warning
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE mml_content
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE mml_reply
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE member_follow
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE ad_notice
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE bs_reply
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE board_qna
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE ad_qna
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

ALTER TABLE mmlr_thumb
	DROP
		PRIMARY KEY
		CASCADE
		KEEP INDEX;

DROP INDEX PK_board_free;

DROP INDEX PK_bf_reply;

DROP INDEX PK_member;

DROP INDEX PK_sns_info;

DROP INDEX PK_movie_info;

DROP INDEX PK_movie_rev;

DROP INDEX PK_cine_info;

DROP INDEX PK_cine_rev;

DROP INDEX PK_bf_thumb;

DROP INDEX PK_sns_code;

DROP INDEX PK_br_thumb;

DROP INDEX PK_board_share;

DROP INDEX PK_ad_member;

DROP INDEX PK_delete_member;

DROP INDEX PK_mr_thumb;

DROP INDEX PK_cr_thumb;

DROP INDEX PK_cr_warning;

DROP INDEX PK_mml_content;

DROP INDEX PK_mml_reply;

DROP INDEX PK_member_follow;

DROP INDEX PK_ad_notice;

DROP INDEX PK_bs_reply;

DROP INDEX PK_board_qna;

DROP INDEX PK_ad_qna;

DROP INDEX PK_mmlr_thumb;

/* board_free */
DROP TABLE board_free 
	CASCADE CONSTRAINTS;

/* bf_reply */
DROP TABLE bf_reply 
	CASCADE CONSTRAINTS;

/* member */
DROP TABLE member 
	CASCADE CONSTRAINTS;

/* sns_info */
DROP TABLE sns_info 
	CASCADE CONSTRAINTS;

/* movie_info */
DROP TABLE movie_info 
	CASCADE CONSTRAINTS;

/* movie_rev */
DROP TABLE movie_rev 
	CASCADE CONSTRAINTS;

/* cine_cinfo */
DROP TABLE cine_info 
	CASCADE CONSTRAINTS;

/* cine_rev */
DROP TABLE cine_rev 
	CASCADE CONSTRAINTS;

/* bf_thumb */
DROP TABLE bf_thumb 
	CASCADE CONSTRAINTS;

/* sns_code */
DROP TABLE sns_code 
	CASCADE CONSTRAINTS;

/* br_thumb */
DROP TABLE br_thumb 
	CASCADE CONSTRAINTS;

/* board_share */
DROP TABLE board_share 
	CASCADE CONSTRAINTS;

/* ad_member */
DROP TABLE ad_member 
	CASCADE CONSTRAINTS;

/* delete_member */
DROP TABLE delete_member 
	CASCADE CONSTRAINTS;

/* free_warning */
DROP TABLE free_warning 
	CASCADE CONSTRAINTS;

/* bs_warning */
DROP TABLE bs_warning 
	CASCADE CONSTRAINTS;

/* mr_thumb */
DROP TABLE mr_thumb 
	CASCADE CONSTRAINTS;

/* mr_warning */
DROP TABLE mr_warning 
	CASCADE CONSTRAINTS;

/* cr_thumb */
DROP TABLE cr_thumb 
	CASCADE CONSTRAINTS;

/* cr_warning */
DROP TABLE cr_warning 
	CASCADE CONSTRAINTS;

/* mml_content */
DROP TABLE mml_content 
	CASCADE CONSTRAINTS;

/* mml_reply */
DROP TABLE mml_reply 
	CASCADE CONSTRAINTS;

/* mml_warning */
DROP TABLE mml_warning 
	CASCADE CONSTRAINTS;

/* mmlr_warning */
DROP TABLE mmlr_warning 
	CASCADE CONSTRAINTS;

/* member_follow */
DROP TABLE member_follow 
	CASCADE CONSTRAINTS;

/* ad_notice */
DROP TABLE ad_notice 
	CASCADE CONSTRAINTS;

/* bfr_warning */
DROP TABLE bfr_warning 
	CASCADE CONSTRAINTS;

/* bs_reply */
DROP TABLE bs_reply 
	CASCADE CONSTRAINTS;

/* sr_warning */
DROP TABLE sr_warning 
	CASCADE CONSTRAINTS;

/* board_qna */
DROP TABLE board_qna 
	CASCADE CONSTRAINTS;

/* ad_qna */
DROP TABLE ad_qna 
	CASCADE CONSTRAINTS;

/* mmlr_thumb */
DROP TABLE mmlr_thumb 
	CASCADE CONSTRAINTS;

/* blacklist */
DROP TABLE blacklist 
	CASCADE CONSTRAINTS;

/* black_spam */
DROP TABLE black_spam 
	CASCADE CONSTRAINTS;

/* board_free */
CREATE TABLE board_free (
	bf_bno NUMBER NOT NULL, /* 자유글번호 */
	id NUMBER NOT NULL, /* 자유작성자 */
	bf_thumb NUMBER, /* 자유추천/비추천 */
	bf_category VARCHAR2(50) NOT NULL, /* 자유카테고리 */
	bf_title VARCHAR2(55) NOT NULL, /* 자유글제목 */
	bf_reg_date DATE NOT NULL, /* 자유등록일 */
	bf_update_date DATE NOT NULL, /* 자유수정일 */
	bf_source VARCHAR2(1000), /* 자유출처 */
	bf_content VARCHAR2(3900) NOT NULL, /* 자유본문 */
	bf_warn_counter NUMBER, /* 자유신고 수 */
	bf_view_counter NUMBER, /* 자유조회수 */
	bf_deleteyn VARCHAR2(2) /* 자유게시글삭제여부 */
);

CREATE UNIQUE INDEX PK_board_free
	ON board_free (
		bf_bno ASC
	);

ALTER TABLE board_free
	ADD
		CONSTRAINT PK_board_free
		PRIMARY KEY (
			bf_bno
		);

/* bf_reply */
CREATE TABLE bf_reply (
	bfr_rno NUMBER NOT NULL, /* 자유댓글번호 */
	bfr_bno NUMBER NOT NULL, /* 자유글번호 */
	id NUMBER NOT NULL, /* 자유댓글작성자 */
	bfr_regdate DATE NOT NULL, /* 자유댓글등록일 */
	bfr_like NUMBER NOT NULL, /* 추천수 */
	bfr_dislike NUMBER NOT NULL, /* 비추천수 */
	bfr_update DATE NOT NULL, /* 자유댓글수정일 */
	bfr_alert NUMBER, /* 자유댓글경고수 */
	bfr_content VARCHAR2(500) NOT NULL, /* 자유댓글내용 */
	bfr_block VARCHAR2(10) /* 자유댓글블락처리여부 */
);

CREATE UNIQUE INDEX PK_bf_reply
	ON bf_reply (
		bfr_rno ASC
	);

ALTER TABLE bf_reply
	ADD
		CONSTRAINT PK_bf_reply
		PRIMARY KEY (
			bfr_rno
		);

/* member */
CREATE TABLE member (
	id NUMBER NOT NULL, /* 멤버ID(시퀀스) */
	m_nickname VARCHAR2(30) NOT NULL, /* 닉네임 */
	m_image VARCHAR2(100), /* 프로필 사진 */
	m_email VARCHAR2(100) NOT NULL, /* 이메일 */
	m_eagree VARCHAR2(2) NOT NULL, /* 이메일 수신동의 */
	m_sagree VARCHAR2(2) NOT NULL, /* SMS수신동의 */
	m_name VARCHAR2(20) NOT NULL, /* 이름 */
	m_phone NUMBER NOT NULL, /* 전화번호 */
	m_cert VARCHAR2(2) NOT NULL, /* 이메일 인증여부 */
	m_password VARCHAR2(40) NOT NULL, /* 패스워드 */
	m_regdate DATE NOT NULL, /* 회원가입일 */
	m_update_date DATE NOT NULL, /* 회원정보 수정일 */
	m_deleteyn VARCHAR2(2) NOT NULL, /* 탈퇴여부 */
	m_following NUMBER NOT NULL, /* 팔로잉수 */
	m_follower NUMBER NOT NULL, /* 팔로워수 */
	m_level VARCHAR2(20) NOT NULL, /* 엠블럼등급 */
	m_favorite VARCHAR2(20), /* 선호장르 */
	m_blacklist VARCHAR2(3) NOT NULL /* 블랙리스트 */
);

CREATE UNIQUE INDEX PK_member
	ON member (
		id ASC
	);

ALTER TABLE member
	ADD
		CONSTRAINT PK_member
		PRIMARY KEY (
			id
		);

/* sns_info */
CREATE TABLE sns_info (
	sns_id NUMBER NOT NULL, /* SNS 고유아이디 */
	id NUMBER NOT NULL, /* SNS멤버ID(시퀀스) */
	sns_code NUMBER NOT NULL, /* SNS코드 */
	sns_connect DATE NOT NULL /* sns연결일시 */
);

CREATE UNIQUE INDEX PK_sns_info
	ON sns_info (
		sns_id ASC
	);

ALTER TABLE sns_info
	ADD
		CONSTRAINT PK_sns_info
		PRIMARY KEY (
			sns_id
		);

/* movie_info */
CREATE TABLE movie_info (
	mi_code NUMBER NOT NULL, /* 영화코드 */
	mi_ktitle VARCHAR2(50) NOT NULL, /* 영화이름 */
	mi_etitle VARCHAR2(50) NOT NULL, /* 영화이름(eng) */
	mi_director VARCHAR2(50) NOT NULL, /* 감독 */
	mi_poster VARCHAR2(300) NOT NULL, /* 포스터 */
	mi_releaseday DATE, /* 개봉일 */
	mi_ccode VARCHAR2(40), /* 국가명 */
	mi_actor VARCHAR2(200), /* 출연배우 */
	mi_story VARCHAR2(1000), /* 줄거리 */
	mi_teaser VARCHAR2(500), /* 티저 */
	grade_code VARCHAR2(20), /* 심의등급 */
	mi_gcode VARCHAR2(20) /* 장르 */
);

CREATE UNIQUE INDEX PK_movie_info
	ON movie_info (
		mi_code ASC
	);

ALTER TABLE movie_info
	ADD
		CONSTRAINT PK_movie_info
		PRIMARY KEY (
			mi_code
		);

/* movie_rev */
CREATE TABLE movie_rev (
	mr_code NUMBER NOT NULL, /* 영화리뷰코드(시퀀스) */
	id NUMBER NOT NULL, /* 영화리뷰작성자 */
	mi_code NUMBER NOT NULL, /* 영화리뷰코드 */
	mr_write_date DATE NOT NULL, /* 영화리뷰작성일 */
	mr_like NUMBER, /* 추천수 */
	mr_dislike NUMBER, /* 비추천수 */
	mr_update_date DATE NOT NULL, /* 영화리뷰수정일 */
	mr_score NUMBER NOT NULL, /* 영화리뷰별점 */
	mr_content VARCHAR2(300) NOT NULL /* 영화리뷰평가내용 */
);

CREATE UNIQUE INDEX PK_movie_rev
	ON movie_rev (
		mr_code ASC
	);

ALTER TABLE movie_rev
	ADD
		CONSTRAINT PK_movie_rev
		PRIMARY KEY (
			mr_code
		);

/* cine_cinfo */
CREATE TABLE cine_info (
	cc_code NUMBER NOT NULL, /* 영화관코드 */
	cc_local_name VARCHAR2(20) NOT NULL, /* 지역이름 */
	cc_brand VARCHAR2(50) NOT NULL, /* 브랜드이름 */
	cc_name  VARCHAR2(50) NOT NULL, /* 영화관 이름 */
	cc_adress VARCHAR2(200) NOT NULL, /* 영화관 주소 */
	cc_link VARCHAR2(200) NOT NULL, /* 영화관 링크 */
	cc_phone VARCHAR2(200) NOT NULL, /* 영화관 전화번호 */
	cc_theaters NUMBER NOT NULL, /* 상영관 수 */
	cc_seats NUMBER NOT NULL, /* 총 좌석수 */
	cc_map_lat NUMBER NOT NULL, /* 위도 */
	cc_map_lon NUMBER NOT NULL, /* 경도 */
	cc_transit VARCHAR2(200) NOT NULL, /* 교통편 */
	cc_parking VARCHAR2(200) NOT NULL, /* 주차 */
	cc_score NUMBER NOT NULL /* 영화관총점 */
);

CREATE UNIQUE INDEX PK_cine_info
	ON cine_info (
		cc_code ASC
	);

ALTER TABLE cine_info
	ADD
		CONSTRAINT PK_cine_info
		PRIMARY KEY (
			cc_code
		);

/* cine_rev */
CREATE TABLE cine_rev (
	cr_code NUMBER NOT NULL, /* 영화관리뷰코드 */
	id NUMBER NOT NULL, /* 리뷰작성자ID(시퀀스) */
	cc_code NUMBER NOT NULL, /* 영화관코드 */
	cr_content VARCHAR2(50) NOT NULL, /* 영화관평가내용 */
	cr_write_date DATE NOT NULL, /* 영화관리뷰작성일자 */
	cr_update_date DATE NOT NULL, /* 영화관리뷰수정일자 */
	cr_score NUMBER NOT NULL /* 영화관점수 */
);

CREATE UNIQUE INDEX PK_cine_rev
	ON cine_rev (
		cr_code ASC
	);

ALTER TABLE cine_rev
	ADD
		CONSTRAINT PK_cine_rev
		PRIMARY KEY (
			cr_code
		);

/* bf_thumb */
CREATE TABLE bf_thumb (
	bf_thumb NUMBER NOT NULL, /* 자유추천/비추천 */
	bf_bno NUMBER NOT NULL, /* 자유글번호 */
	id NUMBER NOT NULL /* 자유추천참여자 */
);

CREATE UNIQUE INDEX PK_bf_thumb
	ON bf_thumb (
		bf_thumb ASC
	);

ALTER TABLE bf_thumb
	ADD
		CONSTRAINT PK_bf_thumb
		PRIMARY KEY (
			bf_thumb
		);

/* sns_code */
CREATE TABLE sns_code (
	sns_code NUMBER NOT NULL /* SNS코드 */
);

CREATE UNIQUE INDEX PK_sns_code
	ON sns_code (
		sns_code ASC
	);

ALTER TABLE sns_code
	ADD
		CONSTRAINT PK_sns_code
		PRIMARY KEY (
			sns_code
		);

/* br_thumb */
CREATE TABLE br_thumb (
	bf_thumb NUMBER NOT NULL, /* 자유댓글추천/비추천 */
	bfr_rno NUMBER NOT NULL, /* 자유댓글번호 */
	id NUMBER NOT NULL /* 자유댓글추천참여자 */
);

CREATE UNIQUE INDEX PK_br_thumb
	ON br_thumb (
		bf_thumb ASC
	);

ALTER TABLE br_thumb
	ADD
		CONSTRAINT PK_br_thumb
		PRIMARY KEY (
			bf_thumb
		);

/* board_share */
CREATE TABLE board_share (
	bs_bno NUMBER NOT NULL, /* 나눔글번호 */
	id NUMBER NOT NULL, /* 나눔작성자 */
	bs_category VARCHAR2(50) NOT NULL, /* 나눔카테고리 */
	bs_content VARCHAR2(3000) NOT NULL, /* 나눔본문 */
	bs_title VARCHAR2(150) NOT NULL, /* 나눔글제목 */
	bs_reg_date DATE NOT NULL, /* 나눔등록일 */
	bs_update_date DATE NOT NULL, /* 나눔수정일 */
	bs_view_counter NUMBER, /* 나눔조회수 */
	bs_warn_counter NUMBER, /* 나눔신고수 */
	bs_deleteyn VARCHAR2(2) /* 나눔글삭제여부 */
);

CREATE UNIQUE INDEX PK_board_share
	ON board_share (
		bs_bno ASC
	);

ALTER TABLE board_share
	ADD
		CONSTRAINT PK_board_share
		PRIMARY KEY (
			bs_bno
		);

/* ad_member */
CREATE TABLE ad_member (
	admin_num NUMBER NOT NULL, /* 관리자번호 */
	admin_id VARCHAR2(20) NOT NULL, /* 관리자ID */
	admin_password VARCHAR2(30) NOT NULL /* 관리자비밀번호 */
);

CREATE UNIQUE INDEX PK_ad_member
	ON ad_member (
		admin_num ASC
	);

ALTER TABLE ad_member
	ADD
		CONSTRAINT PK_ad_member
		PRIMARY KEY (
			admin_num
		);

/* delete_member */
CREATE TABLE delete_member (
	id NUMBER NOT NULL, /* 탈퇴신청멤버ID(시퀀스) */
	delete_date DATE NOT NULL, /* 탈퇴신청날짜 */
	remove_date DATE NOT NULL /* 삭제날짜 */
);

CREATE UNIQUE INDEX PK_delete_member
	ON delete_member (
		id ASC
	);

ALTER TABLE delete_member
	ADD
		CONSTRAINT PK_delete_member
		PRIMARY KEY (
			id
		);

/* free_warning */
CREATE TABLE free_warning (
	bf_bno NUMBER NOT NULL, /* 자유글번호 */
	id NUMBER NOT NULL, /* 신고자 */
	bf_date DATE NOT NULL, /* 신고날짜 */
	bf_warncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

/* bs_warning */
CREATE TABLE bs_warning (
	id NUMBER NOT NULL, /* 나눔신고자 */
	bs_bno NUMBER NOT NULL, /* 나눔글번호 */
	bs_date DATE NOT NULL, /* 신고날짜 */
	bs_warncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

/* mr_thumb */
CREATE TABLE mr_thumb (
	bf_thumb NUMBER NOT NULL, /* 영화리뷰추천/비추천 */
	mr_code NUMBER NOT NULL, /* 영화리뷰코드(시퀀스) */
	id NUMBER NOT NULL /* 영화리뷰ID(시퀀스) */
);

CREATE UNIQUE INDEX PK_mr_thumb
	ON mr_thumb (
		bf_thumb ASC
	);

ALTER TABLE mr_thumb
	ADD
		CONSTRAINT PK_mr_thumb
		PRIMARY KEY (
			bf_thumb
		);

/* mr_warning */
CREATE TABLE mr_warning (
	id NUMBER NOT NULL, /* 영화리뷰신고자 */
	mr_code NUMBER NOT NULL, /* 영화리뷰코드 */
	mr_date DATE NOT NULL, /* 신고날짜 */
	mr_warncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

/* cr_thumb */
CREATE TABLE cr_thumb (
	cr_thumb NUMBER NOT NULL, /* 추천/비추천 */
	id NUMBER NOT NULL, /* 멤버ID(시퀀스) */
	cr_code NUMBER NOT NULL /* 영화관리뷰코드 */
);

CREATE UNIQUE INDEX PK_cr_thumb
	ON cr_thumb (
		cr_thumb ASC
	);

ALTER TABLE cr_thumb
	ADD
		CONSTRAINT PK_cr_thumb
		PRIMARY KEY (
			cr_thumb
		);

/* cr_warning */
CREATE TABLE cr_warning (
	id NUMBER NOT NULL, /* 멤버ID(시퀀스) */
	cr_code NUMBER NOT NULL, /* 영화관리뷰코드 */
	cr_warncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

CREATE UNIQUE INDEX PK_cr_warning
	ON cr_warning (
		id ASC
	);

ALTER TABLE cr_warning
	ADD
		CONSTRAINT PK_cr_warning
		PRIMARY KEY (
			id
		);

/* mml_content */
CREATE TABLE mml_content (
	mml_num NUMBER NOT NULL, /* 나영리코드 */
	mi_code NUMBER NOT NULL, /* 영화코드(여러개 넣을 수 있음) */
	id NUMBER NOT NULL, /* 나영리ID(시퀀스) */
	mml_view_count NUMBER, /* 나영리조회수 */
	mml_write_date DATE NOT NULL, /* 나영리등록일 */
	mml_update_date DATE NOT NULL, /* 나영리수정일 */
	mml_like NUMBER NOT NULL, /* 나영리좋아요 */
	mml_title VARCHAR2(50) NOT NULL, /* 나영리제목 */
	mml_content VARCHAR2(1000) NOT NULL, /* 나영리내용 */
	mml_poster VARCHAR2(3000) NOT NULL, /* 나영리포스터 */
	mml_warn_count NUMBER /* 나영리신고수 */
);

CREATE UNIQUE INDEX PK_mml_content
	ON mml_content (
		mml_num ASC
	);

ALTER TABLE mml_content
	ADD
		CONSTRAINT PK_mml_content
		PRIMARY KEY (
			mml_num
		);

/* mml_reply */
CREATE TABLE mml_reply (
	mml_reply_code NUMBER NOT NULL, /* 나영리리뷰코드 */
	id NUMBER NOT NULL, /* 나영리리뷰ID(시퀀스) */
	mml_num NUMBER NOT NULL, /* 나영리코드 */
	mml_reply_content VARCHAR2(50) NOT NULL, /* 나영리리뷰내용 */
	mml_reply_write_date DATE NOT NULL, /* 나영리리뷰작성일자 */
	mml_reply_update_date DATE NOT NULL, /* 나영리리뷰수정일자 */
	mml_reply_like NUMBER, /* 나영리리뷰추천 */
	mml_reply_dislike NUMBER, /* 나영리리뷰비추천 */
	mml_rep_warn_count NUMBER NOT NULL /* 나영리리뷰신고수 */
);

CREATE UNIQUE INDEX PK_mml_reply
	ON mml_reply (
		mml_reply_code ASC
	);

ALTER TABLE mml_reply
	ADD
		CONSTRAINT PK_mml_reply
		PRIMARY KEY (
			mml_reply_code
		);

/* mml_warning */
CREATE TABLE mml_warning (
	mml_num NUMBER NOT NULL, /* 나영리코드 */
	id NUMBER NOT NULL, /* 나영리신고자ID(시퀀스) */
	mml_date DATE NOT NULL, /* 신고날짜 */
	mml_warncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

/* mmlr_warning */
CREATE TABLE mmlr_warning (
	mml_reply_code NUMBER NOT NULL, /* 나영리리뷰코드 */
	id NUMBER NOT NULL, /* 나영리리뷰ID(시퀀스) */
	mml_reply_date DATE NOT NULL, /* 신고날짜 */
	mml_reply_warncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

/* member_follow */
CREATE TABLE member_follow (
	mf_code NUMBER NOT NULL, /* 팔로잉코드(시퀀스) */
	mf_ing NUMBER NOT NULL, /* 팔로잉 */
	mf_wer NUMBER NOT NULL /* 팔로워 */
);

CREATE UNIQUE INDEX PK_member_follow
	ON member_follow (
		mf_code ASC
	);

ALTER TABLE member_follow
	ADD
		CONSTRAINT PK_member_follow
		PRIMARY KEY (
			mf_code
		);

/* ad_notice */
CREATE TABLE ad_notice (
	an_code NUMBER NOT NULL, /* 관리자공지번호 */
	admin_num NUMBER, /* 관리자번호 */
	an_content VARCHAR2(4000) NOT NULL, /* 관리자공지내용 */
	an_title VARCHAR2(200) NOT NULL, /* 관리자공지제목 */
	an_reg_date DATE NOT NULL, /* 관리자공지작성일 */
	an_update_date DATE NOT NULL /* 관리자공지수정일 */
);

CREATE UNIQUE INDEX PK_ad_notice
	ON ad_notice (
		an_code ASC
	);

ALTER TABLE ad_notice
	ADD
		CONSTRAINT PK_ad_notice
		PRIMARY KEY (
			an_code
		);

/* bfr_warning */
CREATE TABLE bfr_warning (
	bfr_rno NUMBER NOT NULL, /* 자유댓글번호 */
	id NUMBER NOT NULL, /* 신고자 */
	bfr_date DATE NOT NULL /* 신고날짜 */
	bfr_ncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

/* bs_reply */
CREATE TABLE bs_reply (
	bsr_rno NUMBER NOT NULL, /* 나눔댓글번호 */
	bs_bno NUMBER NOT NULL, /* 나눔글번호 */
	id NUMBER NOT NULL, /* 나눔댓글작성자 */
	bsr_regdate DATE NOT NULL, /* 나눔댓글등록일 */
	bsr_update DATE NOT NULL, /* 나눔댓글수정일 */
	bsr_alert NUMBER, /* 나눔댓글경고수 */
	bsr_content VARCHAR2(4000) NOT NULL, /* 나눔댓글내용 */
	bsr_block VARCHAR2(10) /* 블락처리여부 */
);

CREATE UNIQUE INDEX PK_bs_reply
	ON bs_reply (
		bsr_rno ASC
	);

ALTER TABLE bs_reply
	ADD
		CONSTRAINT PK_bs_reply
		PRIMARY KEY (
			bsr_rno
		);

/* bsr_warning */
CREATE TABLE bsr_warning (
	id NUMBER NOT NULL, /* 신고자 */
	bsr_rno NUMBER, /* 나눔댓글번호 */
	bsr_date DATE NOT NULL, /* 신고날짜 */
	bsr_warncontent VARCHAR2(100) NOT NULL /* 신고사유 */
);

/* board_qna */
CREATE TABLE board_qna (
	qna_no NUMBER NOT NULL, /* 문의번호 */
	id NUMBER NOT NULL, /* 문의작성자ID(시퀀스) */
	qna_category VARCHAR2(30) NOT NULL, /* 문의종류 */
	qna_title VARCHAR2(50) NOT NULL, /* 문의제목 */
	qna_content VARCHAR2(1000) NOT NULL, /* 문의내용 */
	qna_date DATE NOT NULL, /* 문의날짜 */
	qna_update_date DATE NOT NULL, /* 문의수정날짜 */
	qna_answer VARCHAR2(10) /* 답변여부 */
);

CREATE UNIQUE INDEX PK_board_qna
	ON board_qna (
		qna_no ASC
	);

ALTER TABLE board_qna
	ADD
		CONSTRAINT PK_board_qna
		PRIMARY KEY (
			qna_no
		);

/* ad_qna */
CREATE TABLE ad_qna (
	aqna_no NUMBER NOT NULL, /* 답변번호 */
	qna_no NUMBER NOT NULL, /* 문의번호 */
	aqna_content VARCHAR2(1000) NOT NULL, /* 답변내용 */
	aqna_date DATE NOT NULL, /* 답변날짜 */
	aqna_update_date DATE NOT NULL, /* 답변수정날짜 */
	admin_num NUMBER /* 관리자번호 */
);

CREATE UNIQUE INDEX PK_ad_qna
	ON ad_qna (
		aqna_no ASC
	);

ALTER TABLE ad_qna
	ADD
		CONSTRAINT PK_ad_qna
		PRIMARY KEY (
			aqna_no
		);

/* mmlr_thumb */
CREATE TABLE mmlr_thumb (
	bf_thumb NUMBER NOT NULL, /* 영화리뷰추천/비추천 */
	id NUMBER NOT NULL, /* 나영리리뷰ID(시퀀스) */
	mml_reply_code NUMBER NOT NULL /* 나영리리뷰코드 */
);

CREATE UNIQUE INDEX PK_mmlr_thumb
	ON mmlr_thumb (
		bf_thumb ASC
	);

ALTER TABLE mmlr_thumb
	ADD
		CONSTRAINT PK_mmlr_thumb
		PRIMARY KEY (
			bf_thumb
		);

/* blacklist */
CREATE TABLE blacklist (
	id NUMBER NOT NULL, /* 블랙ID(시퀀스) */
	black_date DATE NOT NULL /* 등록날짜 */
);

/* black_spam */
CREATE TABLE black_spam (
	spam_number NUMBER NOT NULL, /* 글번호 */
	spam_category VARCHAR2(20) NOT NULL, /* 카테고리 */
	spam_date DATE NOT NULL /* 등록날짜 */
);

ALTER TABLE board_free
	ADD
		CONSTRAINT FK_member_TO_board_free
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE board_free
	ADD
		CONSTRAINT FK_bf_thumb_TO_board_free
		FOREIGN KEY (
			bf_thumb
		)
		REFERENCES bf_thumb (
			bf_thumb
		);

ALTER TABLE bf_reply
	ADD
		CONSTRAINT FK_member_TO_bf_reply
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE bf_reply
	ADD
		CONSTRAINT FK_board_free_TO_bf_reply
		FOREIGN KEY (
			bfr_bno
		)
		REFERENCES board_free (
			bf_bno
		);

ALTER TABLE sns_info
	ADD
		CONSTRAINT FK_sns_code_TO_sns_info
		FOREIGN KEY (
			sns_code
		)
		REFERENCES sns_code (
			sns_code
		);

ALTER TABLE sns_info
	ADD
		CONSTRAINT FK_member_TO_sns_info
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE movie_rev
	ADD
		CONSTRAINT FK_member_TO_movie_rev
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE movie_rev
	ADD
		CONSTRAINT FK_movie_info_TO_movie_rev
		FOREIGN KEY (
			mi_code
		)
		REFERENCES movie_info (
			mi_code
		);

ALTER TABLE cine_rev
	ADD
		CONSTRAINT FK_cine_info_TO_cine_rev
		FOREIGN KEY (
			cc_code
		)
		REFERENCES cine_info (
			cc_code
		);

ALTER TABLE cine_rev
	ADD
		CONSTRAINT cr_thumb
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE bf_thumb
	ADD
		CONSTRAINT FK_board_free_TO_bf_thumb
		FOREIGN KEY (
			bf_bno
		)
		REFERENCES board_free (
			bf_bno
		);

ALTER TABLE bf_thumb
	ADD
		CONSTRAINT FK_member_TO_bf_thumb
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE br_thumb
	ADD
		CONSTRAINT FK_bf_reply_TO_br_thumb
		FOREIGN KEY (
			bfr_rno
		)
		REFERENCES bf_reply (
			bfr_rno
		);

ALTER TABLE br_thumb
	ADD
		CONSTRAINT FK_member_TO_br_thumb
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE board_share
	ADD
		CONSTRAINT FK_member_TO_board_share
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE delete_member
	ADD
		CONSTRAINT FK_member_TO_delete_member
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE free_warning
	ADD
		CONSTRAINT FK_board_free_TO_free_warning
		FOREIGN KEY (
			bf_bno
		)
		REFERENCES board_free (
			bf_bno
		);

ALTER TABLE free_warning
	ADD
		CONSTRAINT FK_member_TO_free_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE bs_warning
	ADD
		CONSTRAINT FK_member_TO_bs_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE bs_warning
	ADD
		CONSTRAINT FK_board_share_TO_bs_warning
		FOREIGN KEY (
			bs_bno
		)
		REFERENCES board_share (
			bs_bno
		);

ALTER TABLE mr_thumb
	ADD
		CONSTRAINT FK_movie_rev_TO_mr_thumb
		FOREIGN KEY (
			mr_code
		)
		REFERENCES movie_rev (
			mr_code
		);

ALTER TABLE mr_thumb
	ADD
		CONSTRAINT FK_member_TO_mr_thumb
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE mr_warning
	ADD
		CONSTRAINT FK_member_TO_mr_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE mr_warning
	ADD
		CONSTRAINT FK_movie_rev_TO_mr_warning
		FOREIGN KEY (
			mr_code
		)
		REFERENCES movie_rev (
			mr_code
		);

ALTER TABLE cr_thumb
	ADD
		CONSTRAINT FK_member_TO_cr_thumb
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE cr_thumb
	ADD
		CONSTRAINT FK_cine_rev_TO_cr_thumb
		FOREIGN KEY (
			cr_code
		)
		REFERENCES cine_rev (
			cr_code
		);

ALTER TABLE cr_warning
	ADD
		CONSTRAINT FK_member_TO_cr_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE cr_warning
	ADD
		CONSTRAINT FK_cine_rev_TO_cr_warning
		FOREIGN KEY (
			cr_code
		)
		REFERENCES cine_rev (
			cr_code
		);

ALTER TABLE mml_content
	ADD
		CONSTRAINT FK_member_TO_mml_content
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE mml_content
	ADD
		CONSTRAINT FK_movie_info_TO_mml_content
		FOREIGN KEY (
			mi_code
		)
		REFERENCES movie_info (
			mi_code
		);

ALTER TABLE mml_reply
	ADD
		CONSTRAINT FK_member_TO_mml_reply
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE mml_reply
	ADD
		CONSTRAINT FK_mml_content_TO_mml_reply
		FOREIGN KEY (
			mml_num
		)
		REFERENCES mml_content (
			mml_num
		);

ALTER TABLE mml_warning
	ADD
		CONSTRAINT FK_mml_content_TO_mml_warning
		FOREIGN KEY (
			mml_num
		)
		REFERENCES mml_content (
			mml_num
		);

ALTER TABLE mml_warning
	ADD
		CONSTRAINT FK_member_TO_mml_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE mmlr_warning
	ADD
		CONSTRAINT FK_mml_reply_TO_mmlr_warning
		FOREIGN KEY (
			mml_reply_code
		)
		REFERENCES mml_reply (
			mml_reply_code
		);

ALTER TABLE mmlr_warning
	ADD
		CONSTRAINT FK_member_TO_mmlr_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE member_follow
	ADD
		CONSTRAINT FK_member_TO_member_follow
		FOREIGN KEY (
			mf_ing
		)
		REFERENCES member (
			id
		);

ALTER TABLE member_follow
	ADD
		CONSTRAINT FK_member_TO_member_follow2
		FOREIGN KEY (
			mf_wer
		)
		REFERENCES member (
			id
		);

ALTER TABLE ad_notice
	ADD
		CONSTRAINT FK_ad_member_TO_ad_notice
		FOREIGN KEY (
			admin_num
		)
		REFERENCES ad_member (
			admin_num
		);

ALTER TABLE bfr_warning
	ADD
		CONSTRAINT FK_member_TO_bfr_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE bfr_warning
	ADD
		CONSTRAINT FK_bf_reply_TO_bfr_warning
		FOREIGN KEY (
			bfr_rno
		)
		REFERENCES bf_reply (
			bfr_rno
		);

ALTER TABLE bs_reply
	ADD
		CONSTRAINT FK_board_share_TO_bs_reply
		FOREIGN KEY (
			bs_bno
		)
		REFERENCES board_share (
			bs_bno
		);

ALTER TABLE bs_reply
	ADD
		CONSTRAINT FK_member_TO_bs_reply
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE sr_warning
	ADD
		CONSTRAINT FK_member_TO_sr_warning
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE sr_warning
	ADD
		CONSTRAINT FK_bs_reply_TO_sr_warning
		FOREIGN KEY (
			bsr_rno
		)
		REFERENCES bs_reply (
			bsr_rno
		);

ALTER TABLE board_qna
	ADD
		CONSTRAINT FK_member_TO_board_qna
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE ad_qna
	ADD
		CONSTRAINT FK_board_qna_TO_ad_qna
		FOREIGN KEY (
			qna_no
		)
		REFERENCES board_qna (
			qna_no
		);

ALTER TABLE ad_qna
	ADD
		CONSTRAINT FK_ad_member_TO_ad_qna
		FOREIGN KEY (
			admin_num
		)
		REFERENCES ad_member (
			admin_num
		);

ALTER TABLE mmlr_thumb
	ADD
		CONSTRAINT FK_member_TO_mmlr_thumb
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

ALTER TABLE mmlr_thumb
	ADD
		CONSTRAINT FK_mml_reply_TO_mmlr_thumb
		FOREIGN KEY (
			mml_reply_code
		)
		REFERENCES mml_reply (
			mml_reply_code
		);

ALTER TABLE blacklist
	ADD
		CONSTRAINT FK_member_TO_blacklist
		FOREIGN KEY (
			id
		)
		REFERENCES member (
			id
		);

/* 시퀀스 생성문 */
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
create sequence seq_member_id
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
```
```

0807 수정완료
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
create sequence seq_member_id
   start with 1
   increment by 1
   nomaxvalue
   nocycle;
```
0807 수정완료
/* 2. (필요시) 시퀀스 삭제문

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
*/

0807 수정완료
# 3. MML_CONTENT 테이블 수정사항입니다.
1. member : m_image VARCHAR(100)<크기 늘림>
2. movie_info : mi_story VARCHAR2(1000)<크기늘림>  
3. movie_rev : mi_code NUMBER NOT NULL, / **영화고유코드**/<주석변경>  
4. mml_content : mi_code VARCHAR(100) NOT NULL, /* 영화코드(여러개 넣을 수 있음) */  
5. 각각의 신고테이블에 신고사유 받을 수 있게 컬럼 추가하는것도 좋을거같아용(warn_content) 
6. FK_movie_info_TO_mml_content 는 만들지 않는게 좋을거같아용(이거를 생성하면 mml_content의 mi_code에 영화코드 1개만 넣을 수 있음)
mml_content수정사항에 4번 6번 있습니당!  
나중에 db생성문에서 아예 적용해주는것도 좋을것 같습니댱

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

# 5. 트리거 추가(board_qna삭제시 admin_qna삭제)
```
create or replace trigger boardQna_to_adQna_delete
before delete on BOARD_QNA for each row
begin
delete AD_QNA where qna_no = :old.qna_no;
end;
/
```

# 6. movie_info 테이블의 mi_gcode 20에서 50으로 크기 늘렸습니다
- movie_info : mi_gcode(20) -> (50)

# 7. movie_info 에 상영시간 칼럼이 없네MI_TIME 칼럼 추가

- movie_info : MI_TIME (상영시간) 컬럼 추가

# 8. movie_rev 테이블에 신고수 칼럼이 없네요. mr_alert 추가

- movie_rev : mr_alert 추가
```
```
# 9. mr_thumb의 bf_thumb pk 제거

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA3OTQ3Mjc4MywxOTI5NzQzMzYyLC02OD
U3ODg3NTIsODA1Njc4NjcyLC00OTUxOTk5MDcsLTEwMTYyMDY1
MTMsNjcyMjcxODA5LDEwNjk5ODQwNTgsLTM4ODMwNzc4M119
-->