/**
 * 🚀 Debug Logger 사용 가이드
 * 
 * 이 프로젝트는 개발 환경에서만 디버그 로그를 출력하도록 설정되어 있습니다.
 * Production 환경에서는 npm run dev로 실행해도 로그가 출력되지 않습니다.
 * 
 * === 기본 동작 ===
 * - 개발 환경 (localhost, 127.0.0.1, 192.168.x.x 등): 디버그 로그 출력 ✅
 * - 프로덕션 환경 (실제 도메인): 디버그 로그 숨김 ❌
 * - npm run dev로 프로덕션 서버에서 실행해도 로그 숨김 ❌
 * 
 * === 브라우저에서 수동 제어 ===
 * 개발 모드에서도 로그를 끄거나, 프로덕션에서도 로그를 켜고 싶다면:
 * 
 * 브라우저 콘솔에서 다음 명령어 사용:
 * 
 * // 로그 켜기 (환경 관계없이 강제 활성화)
 * enableDebugLogs()
 * 
 * // 로그 끄기 (환경 관계없이 강제 비활성화)  
 * disableDebugLogs()
 * 
 * // 기본값으로 리셋 (환경에 따른 자동 설정)
 * resetDebugLogs()
 * 
 * // 현재 환경 정보 확인
 * checkEnvironment()
 * 
 * === 코드에서 사용법 ===
 * 
 * import { devLog, prodLog } from '@/app/utils/logger';
 * 
 * // 개발 환경에서만 출력되는 로그
 * devLog.log('디버그 정보');
 * devLog.error('개발용 에러');
 * devLog.warn('개발용 경고');
 * devLog.info('개발용 정보');
 * 
 * // 항상 출력되는 로그 (중요한 에러용)
 * prodLog.error('심각한 에러'); 
 * prodLog.warn('중요한 경고');
 * 
 * === 적용된 파일들 ===
 * - Canvas.jsx: 캔버스 상태 변경, 노드/엣지 로딩 등
 * - page.tsx: 워크플로우 저장/복원, 메뉴 상태 등  
 * - Node.jsx: 노드 파라미터 변경, 이벤트 처리 등
 * - TemplatePanel.jsx: 템플릿 로딩, 미리보기 등
 * - TemplatePreview.jsx: 팝업 상호작용 등
 * - workflowStorage.js: localStorage 저장/로드 등
 * 
 * === 테스트 방법 ===
 * 1. npm run dev로 실행 → 로그 확인
 * 2. 브라우저에서 disableDebugLogs() 실행 → 로그 사라짐
 * 3. enableDebugLogs() 실행 → 로그 다시 나타남
 * 4. npm run build → npm start로 프로덕션 모드 테스트
 */

console.log('🎯 Debug Logger가 활성화되었습니다!');
console.log('브라우저 콘솔에서 enableDebugLogs(), disableDebugLogs(), resetDebugLogs() 함수를 사용할 수 있습니다.');
