# Todo App with Next.js and Supabase

이 프로젝트는 Next.js와 Supabase를 사용하여 만든 할 일 관리 애플리케이션입니다.

## 기능

- 할 일 목록 조회
- 새 할 일 추가
- 할 일 완료/미완료 상태 변경
- 할 일 내용 수정
- 할 일 삭제
- 필터링 (전체/미완료/완료)

## 기술 스택

- **Frontend**: Next.js, React, TypeScript, Tailwind CSS, shadcn/ui
- **Backend**: Supabase (PostgreSQL 데이터베이스)
- **상태 관리**: React Hooks
- **애니메이션**: Framer Motion
- **아이콘**: Lucide React

## 설치 및 실행 방법

1. 저장소 클론
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. 의존성 설치
   ```bash
   npm install
   ```

3. 환경 변수 설정
   `.env.local` 파일을 생성하고 다음 내용을 추가합니다:
   ```
   NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. 개발 서버 실행
   ```bash
   npm run dev
   ```

5. 브라우저에서 `http://localhost:3000` 접속

## Supabase 설정

1. [Supabase](https://supabase.com/)에서 새 프로젝트 생성
2. SQL 에디터에서 다음 쿼리 실행:
   ```sql
   CREATE TABLE todos (
     id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
     task TEXT NOT NULL,
     is_completed BOOLEAN DEFAULT FALSE,
     created_at TIMESTAMPTZ DEFAULT NOW(),
     updated_at TIMESTAMPTZ DEFAULT NOW(),
     user_id UUID
   );
   ```
3. Row Level Security (RLS) 설정 (선택 사항)

## 배포

이 프로젝트는 Vercel에 쉽게 배포할 수 있습니다:

1. [Vercel](https://vercel.com)에 GitHub 저장소 연결
2. 환경 변수 설정
3. 배포 완료!

## 라이선스

MIT

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
#   m y s p a c e 
 
 