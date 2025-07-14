<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>K-팝 세계로의 여행</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    animation: {
                        'fade-in': 'fadeIn 0.8s ease-out forwards',
                        'fade-in-up': 'fadeInUp 0.8s ease-out forwards',
                        'fade-in-down': 'fadeInDown 0.8s ease-out forwards',
                        'fade-in-left': 'fadeInLeft 0.8s ease-out forwards',
                        'fade-in-right': 'fadeInRight 0.8s ease-out forwards',
                        'slide-up': 'slideUp 0.6s ease-out',
                        'float': 'float 4s ease-in-out infinite',
                        'glow': 'glow 2s ease-in-out infinite alternate',
                        'shimmer': 'shimmer 2s linear infinite',
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' },
                        },
                        fadeInUp: {
                            '0%': { opacity: '0', transform: 'translateY(30px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        },
                        fadeInDown: {
                            '0%': { opacity: '0', transform: 'translateY(-30px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        },
                        fadeInLeft: {
                            '0%': { opacity: '0', transform: 'translateX(-30px)' },
                            '100%': { opacity: '1', transform: 'translateX(0)' },
                        },
                        fadeInRight: {
                            '0%': { opacity: '0', transform: 'translateX(30px)' },
                            '100%': { opacity: '1', transform: 'translateX(0)' },
                        },
                        slideUp: {
                            '0%': { transform: 'translateY(20px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' },
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-15px)' },
                        },
                        glow: {
                            '0%': { boxShadow: '0 0 20px rgba(255, 182, 193, 0.5)' },
                            '100%': { boxShadow: '0 0 30px rgba(255, 182, 193, 0.8)' },
                        },
                        shimmer: {
                            '0%': { transform: 'translateX(-100%)' },
                            '100%': { transform: 'translateX(100%)' },
                        }
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&display=swap');
        body { font-family: 'Noto Sans KR', sans-serif; }
        
        .glass {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .glass-strong {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        .glass-card {
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.15);
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 25%, #f093fb 50%, #f5576c 75%, #4facfe 100%);
        }
        
        .text-shadow {
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        /* 초기 상태 - 숨김 */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
        }

        /* 애니메이션 완료 후 상태 */
        .animate-on-scroll.animate {
            opacity: 1;
            transform: translateY(0);
            transition: all 0.8s ease-out;
        }

        /* 지연 시간 클래스들 */
        .delay-100 { animation-delay: 0.1s; }
        .delay-200 { animation-delay: 0.2s; }
        .delay-300 { animation-delay: 0.3s; }
        .delay-400 { animation-delay: 0.4s; }
        .delay-500 { animation-delay: 0.5s; }
        .delay-600 { animation-delay: 0.6s; }
        .delay-700 { animation-delay: 0.7s; }
        .delay-800 { animation-delay: 0.8s; }
        .delay-900 { animation-delay: 0.9s; }
        .delay-1000 { animation-delay: 1s; }
    </style>
</head>
<body class="gradient-bg min-h-screen relative overflow-x-hidden">
    <!-- Animated Background -->
    <div class="fixed inset-0 overflow-hidden pointer-events-none">
        <div class="absolute -top-40 -right-40 w-80 h-80 bg-white/5 rounded-full blur-3xl animate-float"></div>
        <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-white/5 rounded-full blur-3xl animate-float" style="animation-delay: 2s;"></div>
        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-white/3 rounded-full blur-3xl animate-float" style="animation-delay: 4s;"></div>
    </div>

    <!-- Hero Section -->
    <div class="relative z-10 container mx-auto px-4 py-16">
        <div class="text-center">
            <!-- Korean Flag -->
            <div class="flex justify-center mb-8 animate-fade-in-down delay-100">
                <div class="glass-strong rounded-2xl p-6 shadow-2xl">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/0/09/Flag_of_South_Korea.svg" 
                         alt="대한민국 국기" 
                         class="w-24 h-16 object-contain rounded-lg shadow-lg">
                    <p class="text-white text-sm mt-2 font-medium">Made in Korea 🇰🇷</p>
                </div>
            </div>
            
            <h1 class="text-6xl md:text-8xl font-bold mb-6 text-white text-shadow animate-fade-in delay-300">
                🎵 K-팝 🎵
            </h1>
            <p class="text-xl md:text-2xl text-white/90 mb-8 font-medium text-shadow animate-fade-in delay-400">
                한국의 음악이 전 세계를 사로잡다
            </p>
            
            <div class="flex justify-center space-x-4 mb-8 animate-fade-in delay-500">
                <div class="w-3 h-3 bg-white rounded-full animate-pulse"></div>
                <div class="w-3 h-3 bg-white/70 rounded-full animate-pulse" style="animation-delay: 0.2s;"></div>
                <div class="w-3 h-3 bg-white/50 rounded-full animate-pulse" style="animation-delay: 0.4s;"></div>
            </div>
            
            <div class="glass-strong rounded-3xl p-8 max-w-3xl mx-auto shadow-2xl animate-fade-in-up delay-600">
                <p class="text-lg text-white/90 leading-relaxed">
                    K-팝은 대한민국에서 시작되어 전 세계를 사로잡은 문화 현상입니다. 
                    음악, 댄스, 패션, 팬덤 문화가 결합된 종합 엔터테인먼트를 경험해보세요!
                </p>
            </div>
        </div>
    </div>

    <!-- Main Content -->
    <div class="container mx-auto px-4 py-16 relative z-10">
        <!-- What is K-pop Section -->
        <div class="max-w-4xl mx-auto mb-20 animate-fade-in-up delay-700">
            <div class="glass-strong rounded-3xl p-8 md:p-12 shadow-2xl border border-white/20">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-8 text-center text-shadow animate-fade-in delay-800">
                    🌟 K-팝이란?
                </h2>
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="space-y-4 animate-fade-in-left delay-900">
                        <p class="text-white/90 text-lg leading-relaxed">
                            K-팝(Korean Pop)은 대한민국의 대중음악을 의미하는 용어입니다. 1990년대 후반부터 시작되어 2010년대 이후 전 세계적으로 큰 인기를 얻고 있는 문화 현상입니다.
                        </p>
                        <p class="text-white/90 text-lg leading-relaxed">
                            K-팝은 단순한 음악 장르를 넘어서 패션, 댄스, 뮤직비디오, 팬덤 문화 등이 결합된 종합 엔터테인먼트 산업으로 발전했습니다.
                        </p>
                        <p class="text-white/90 text-lg leading-relaxed">
                            특히 2010년대 이후 BTS, BLACKPINK 등의 글로벌 성공으로 K-팝은 세계 음악 시장의 주요 플레이어로 자리매김했습니다.
                        </p>
                    </div>
                    <div class="glass-card rounded-2xl p-6 border border-pink-300/30 animate-fade-in-right delay-1000">
                        <h3 class="text-2xl font-bold text-white mb-4">🎯 핵심 특징</h3>
                        <ul class="space-y-3 text-white/80">
                            <li class="flex items-center">
                                <span class="w-2 h-2 bg-pink-400 rounded-full mr-3"></span>
                                완벽한 퍼포먼스와 안무
                            </li>
                            <li class="flex items-center">
                                <span class="w-2 h-2 bg-purple-400 rounded-full mr-3"></span>
                                독특한 컨셉과 스토리텔링
                            </li>
                            <li class="flex items-center">
                                <span class="w-2 h-2 bg-cyan-400 rounded-full mr-3"></span>
                                글로벌 팬덤 문화
                            </li>
                            <li class="flex items-center">
                                <span class="w-2 h-2 bg-yellow-400 rounded-full mr-3"></span>
                                체계적인 트레이닝 시스템
                            </li>
                            <li class="flex items-center">
                                <span class="w-2 h-2 bg-green-400 rounded-full mr-3"></span>
                                소셜미디어 활용
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- K-pop History Section -->
        <div class="max-w-6xl mx-auto mb-20">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-12 text-center text-shadow animate-fade-in delay-100">
                📚 K-팝의 역사
            </h2>
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div class="group animate-fade-in-up delay-200">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-blue-300/30">
                        <div class="text-center">
                            <div class="text-4xl mb-3">🎵</div>
                            <h4 class="text-xl font-bold text-white mb-2">1990년대</h4>
                            <p class="text-white/70 text-sm">서태지와 아이들, H.O.T, 젝스키스 등 1세대 아이돌 그룹의 등장으로 K-팝의 기반 형성</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-300">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-purple-300/30">
                        <div class="text-center">
                            <div class="text-4xl mb-3">🌟</div>
                            <h4 class="text-xl font-bold text-white mb-2">2000년대</h4>
                            <p class="text-white/70 text-sm">동방신기, 슈퍼주니어, 소녀시대 등 2세대 아이돌의 전성기, 아시아 시장 진출</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-400">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-pink-300/30">
                        <div class="text-center">
                            <div class="text-4xl mb-3">🌍</div>
                            <h4 class="text-xl font-bold text-white mb-2">2010년대</h4>
                            <p class="text-white/70 text-sm">BTS, BLACKPINK, EXO 등 3세대 아이돌의 글로벌 성공, 세계 시장 진출</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-500">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-green-300/30">
                        <div class="text-center">
                            <div class="text-4xl mb-3">🚀</div>
                            <h4 class="text-xl font-bold text-white mb-2">2020년대</h4>
                            <p class="text-white/70 text-sm">뉴진스, IVE, LE SSERAFIM 등 4세대 아이돌, 디지털 시대의 새로운 트렌드</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- K-pop Industry Section -->
        <div class="max-w-4xl mx-auto mb-20 animate-fade-in-up delay-600">
            <div class="glass-strong rounded-3xl p-8 md:p-12 shadow-2xl border border-white/20">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-8 text-center text-shadow animate-fade-in delay-700">
                    🏢 K-팝 산업
                </h2>
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="space-y-6">
                        <div class="glass-card rounded-2xl p-6 border border-blue-300/30">
                            <h3 class="text-2xl font-bold text-white mb-3">🎯 주요 기획사</h3>
                            <div class="space-y-3 text-white/80">
                                <div class="flex items-center justify-between">
                                    <span>HYBE (구 Big Hit)</span>
                                    <span class="bg-purple-500/20 px-2 py-1 rounded text-sm">BTS, 뉴진스</span>
                                </div>
                                <div class="flex items-center justify-between">
                                    <span>SM Entertainment</span>
                                    <span class="bg-blue-500/20 px-2 py-1 rounded text-sm">EXO, Red Velvet</span>
                                </div>
                                <div class="flex items-center justify-between">
                                    <span>JYP Entertainment</span>
                                    <span class="bg-pink-500/20 px-2 py-1 rounded text-sm">TWICE, Stray Kids</span>
                                </div>
                                <div class="flex items-center justify-between">
                                    <span>YG Entertainment</span>
                                    <span class="bg-black/20 px-2 py-1 rounded text-sm">BLACKPINK, TREASURE</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="space-y-6">
                        <div class="glass-card rounded-2xl p-6 border border-green-300/30">
                            <h3 class="text-2xl font-bold text-white mb-3">💰 산업 규모</h3>
                            <div class="space-y-3 text-white/80">
                                <div class="flex items-center justify-between">
                                    <span>글로벌 시장 규모</span>
                                    <span class="bg-green-500/20 px-2 py-1 rounded text-sm">100억 달러+</span>
                                </div>
                                <div class="flex items-center justify-between">
                                    <span>수출 규모</span>
                                    <span class="bg-blue-500/20 px-2 py-1 rounded text-sm">연간 증가</span>
                                </div>
                                <div class="flex items-center justify-between">
                                    <span>고용 창출</span>
                                    <span class="bg-purple-500/20 px-2 py-1 rounded text-sm">수만 명</span>
                                </div>
                                <div class="flex items-center justify-between">
                                    <span>관광 효과</span>
                                    <span class="bg-pink-500/20 px-2 py-1 rounded text-sm">한류 관광</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Features Section -->
        <div class="max-w-6xl mx-auto mb-20">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-12 text-center text-shadow animate-fade-in delay-100">
                ✨ K-팝의 특징
            </h2>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="group animate-fade-in-up delay-200">
                    <div class="glass-strong rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 hover:scale-105 border border-white/20">
                        <div class="text-5xl mb-4 text-center">🎭</div>
                        <h3 class="text-2xl font-bold text-white mb-4 text-center">완벽한 퍼포먼스</h3>
                        <p class="text-white/80 leading-relaxed text-center">
                            정교한 안무와 화려한 무대 연출로 시각적 즐거움을 제공합니다. 수백 시간의 연습을 통해 완성되는 완벽한 동기화와 표현력이 K-팝의 핵심입니다.
                        </p>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-400">
                    <div class="glass-strong rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 hover:scale-105 border border-white/20">
                        <div class="text-5xl mb-4 text-center">🎨</div>
                        <h3 class="text-2xl font-bold text-white mb-4 text-center">독특한 컨셉</h3>
                        <p class="text-white/80 leading-relaxed text-center">
                            매번 새로운 테마와 스토리텔링으로 팬들을 매료시킵니다. 음악, 패션, 뮤직비디오가 하나의 아트워크로 완성되는 독창적인 세계관을 구축합니다.
                        </p>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-600">
                    <div class="glass-strong rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 hover:scale-105 border border-white/20">
                        <div class="text-5xl mb-4 text-center">🌍</div>
                        <h3 class="text-2xl font-bold text-white mb-4 text-center">글로벌 영향력</h3>
                        <p class="text-white/80 leading-relaxed text-center">
                            전 세계 팬들과 소통하며 문화 교류의 다리 역할을 합니다. 언어의 장벽을 넘어 음악과 감정으로 연결되는 글로벌 팬덤 문화를 만들어냅니다.
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <!-- K-pop Culture Section -->
        <div class="max-w-4xl mx-auto mb-20 animate-fade-in-up delay-700">
            <div class="glass-strong rounded-3xl p-8 md:p-12 shadow-2xl border border-white/20">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-8 text-center text-shadow animate-fade-in delay-800">
                    🎪 K-팝 문화
                </h2>
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="space-y-6">
                        <div class="glass-card rounded-2xl p-6 border border-pink-300/30">
                            <h3 class="text-2xl font-bold text-white mb-3">💖 팬덤 문화</h3>
                            <div class="space-y-3 text-white/80">
                                <p class="text-sm">K-팝 팬덤은 전 세계적으로 가장 열정적이고 조직적인 팬 문화를 가지고 있습니다.</p>
                                <ul class="text-sm space-y-2">
                                    <li>• 팬클럽 활동과 팬미팅</li>
                                    <li>• 소셜미디어 팔로워십</li>
                                    <li>• 콘서트와 팬사인회</li>
                                    <li>• 팬아트와 팬픽션</li>
                                </ul>
                            </div>
                        </div>
                        <div class="glass-card rounded-2xl p-6 border border-blue-300/30">
                            <h3 class="text-2xl font-bold text-white mb-3">🎵 음악적 특징</h3>
                            <div class="space-y-3 text-white/80">
                                <p class="text-sm">K-팝은 다양한 장르를 융합한 독특한 음악 스타일을 가지고 있습니다.</p>
                                <ul class="text-sm space-y-2">
                                    <li>• 팝, 힙합, R&B의 융합</li>
                                    <li>• 전자음악과 EDM 요소</li>
                                    <li>• 다국어 가사 활용</li>
                                    <li>• 후크 중심의 메인 멜로디</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="space-y-6">
                        <div class="glass-card rounded-2xl p-6 border border-purple-300/30">
                            <h3 class="text-2xl font-bold text-white mb-3">🎬 뮤직비디오</h3>
                            <div class="space-y-3 text-white/80">
                                <p class="text-sm">K-팝 뮤직비디오는 영화적 퀄리티와 독창적인 스토리텔링으로 유명합니다.</p>
                                <ul class="text-sm space-y-2">
                                    <li>• 고퀄리티 영상 제작</li>
                                    <li>• 독창적인 컨셉과 스토리</li>
                                    <li>• 패션과 뷰티 트렌드</li>
                                    <li>• 글로벌 감각의 연출</li>
                                </ul>
                            </div>
                        </div>
                        <div class="glass-card rounded-2xl p-6 border border-green-300/30">
                            <h3 class="text-2xl font-bold text-white mb-3">📱 디지털 시대</h3>
                            <div class="space-y-3 text-white/80">
                                <p class="text-sm">소셜미디어와 스트리밍 플랫폼을 활용한 새로운 소통 방식</p>
                                <ul class="text-sm space-y-2">
                                    <li>• YouTube와 TikTok 활용</li>
                                    <li>• 실시간 팬과의 소통</li>
                                    <li>• 글로벌 스트리밍 차트</li>
                                    <li>• 디지털 마케팅 혁신</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Artists Section -->
        <div class="max-w-7xl mx-auto mb-20">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-12 text-center text-shadow animate-fade-in delay-100">
                👑 대표적인 K-팝 아티스트
            </h2>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="group animate-fade-in-up delay-200">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-pink-300/30">
                        <div class="text-center">
                            <div class="text-3xl mb-3">💜</div>
                            <h4 class="text-xl font-bold text-white mb-2">BTS (방탄소년단)</h4>
                            <p class="text-white/70 text-sm">글로벌 슈퍼스타로 K-팝을 세계 무대에 올린 그룹</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-300">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-pink-300/30">
                        <div class="text-center">
                            <div class="text-3xl mb-3">🖤</div>
                            <h4 class="text-xl font-bold text-white mb-2">BLACKPINK</h4>
                            <p class="text-white/70 text-sm">강력한 퍼포먼스와 독보적인 스타일로 인기</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-400">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-pink-300/30">
                        <div class="text-center">
                            <div class="text-3xl mb-3">💖</div>
                            <h4 class="text-xl font-bold text-white mb-2">TWICE</h4>
                            <p class="text-white/70 text-sm">상큼하고 귀여운 매력으로 아시아 팬들의 사랑</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-500">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-blue-300/30">
                        <div class="text-center">
                            <div class="text-3xl mb-3">💎</div>
                            <h4 class="text-xl font-bold text-white mb-2">EXO</h4>
                            <p class="text-white/70 text-sm">완벽한 보컬과 댄스로 K-팝의 정석을 보여주는 그룹</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-600">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-red-300/30">
                        <div class="text-center">
                            <div class="text-3xl mb-3">❤️</div>
                            <h4 class="text-xl font-bold text-white mb-2">Red Velvet</h4>
                            <p class="text-white/70 text-sm">독특한 컨셉과 실험적인 음악으로 주목받는 그룹</p>
                        </div>
                    </div>
                </div>
                <div class="group animate-fade-in-up delay-700">
                    <div class="glass-card rounded-3xl p-6 shadow-xl hover:shadow-2xl transition-all duration-500 hover:scale-105 border border-teal-300/30">
                        <div class="text-center">
                            <div class="text-3xl mb-3">💎</div>
                            <h4 class="text-xl font-bold text-white mb-2">SEVENTEEN</h4>
                            <p class="text-white/70 text-sm">자체 제작 아이돌로 음악과 안무를 직접 만드는 그룹</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Cultural Impact Section -->
        <div class="max-w-4xl mx-auto mb-20 animate-fade-in-up delay-800">
            <div class="glass-strong rounded-3xl p-8 md:p-12 shadow-2xl border border-white/20">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-8 text-center text-shadow animate-fade-in delay-900">
                    🎪 K-팝의 문화적 영향
                </h2>
                <div class="space-y-6 text-white/90 text-lg">
                    <p class="animate-fade-in-left delay-1000">
                        K-팝은 단순한 음악을 넘어서 한국의 문화를 전 세계에 알리는 중요한 매개체 역할을 하고 있습니다. 한류(Korean Wave)의 핵심 동력으로서 한국의 패션, 뷰티, 음식, 언어 등 다양한 문화 요소들을 함께 전파하고 있습니다.
                    </p>
                    
                    <div class="glass-card rounded-2xl p-6 border border-pink-300/50 text-center animate-fade-in delay-1100">
                        <p class="text-2xl font-bold text-white">
                            💫 K-팝은 음악을 통해 세계와 한국을 연결하는 문화의 다리입니다! 💫
                        </p>
                    </div>

                    <p class="animate-fade-in-right delay-1200">
                        K-팝의 성공은 체계적인 트레이닝 시스템, 혁신적인 마케팅 전략, 그리고 팬들과의 적극적인 소통 덕분입니다. 특히 소셜미디어를 활용한 글로벌 팬덤 문화는 K-팝만의 독특한 특징입니다.
                    </p>
                </div>
            </div>
        </div>

        <!-- Latest K-pop News Section -->
        <div class="max-w-6xl mx-auto mb-20">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-12 text-center text-shadow animate-fade-in delay-100">
                📰 최신 K-팝 뉴스
            </h2>
            <div class="grid md:grid-cols-2 gap-8">
                <!-- KPop Demon Hunters News -->
                <div class="group animate-fade-in-up delay-200">
                    <div class="glass-strong rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 hover:scale-105 border border-white/20">
                        <div class="text-5xl mb-4 text-center">🎬</div>
                        <h3 class="text-2xl font-bold text-white mb-4 text-center">KPop Demon Hunters</h3>
                        <p class="text-white/80 leading-relaxed text-center mb-4">
                            넷플릭스 애니메이션 영화 'KPop Demon Hunters'가 글로벌 차트를 석권하고 있습니다!
                        </p>
                        <div class="space-y-3 text-white/70 text-sm">
                            <div class="flex items-center justify-between">
                                <span>🏆 Billboard Hot 100 진입</span>
                                <span class="bg-pink-500/20 px-2 py-1 rounded">8곡</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>📈 Billboard 200 순위</span>
                                <span class="bg-purple-500/20 px-2 py-1 rounded">3위</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>🎵 Spotify US 차트</span>
                                <span class="bg-blue-500/20 px-2 py-1 rounded">1위</span>
                            </div>
                        </div>
                        <div class="mt-4 p-3 bg-gradient-to-r from-pink-500/20 to-purple-500/20 rounded-xl border border-pink-300/30">
                            <p class="text-white/90 text-sm text-center">
                                "Golden" - 가상 걸그룹 HUNTR/X의 메인 테마곡이 오스카 후보로 거론되고 있습니다!
                            </p>
                        </div>
                    </div>
                </div>

                <!-- BTS Comeback News -->
                <div class="group animate-fade-in-up delay-400">
                    <div class="glass-strong rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 hover:scale-105 border border-white/20">
                        <div class="text-5xl mb-4 text-center">💜</div>
                        <h3 class="text-2xl font-bold text-white mb-4 text-center">BTS 컴백 소식</h3>
                        <p class="text-white/80 leading-relaxed text-center mb-4">
                            글로벌 슈퍼스타 BTS가 4년 만에 완전체로 돌아옵니다!
                        </p>
                        <div class="space-y-3 text-white/70 text-sm">
                            <div class="flex items-center justify-between">
                                <span>📅 새 앨범 발매</span>
                                <span class="bg-purple-500/20 px-2 py-1 rounded">2026년 봄</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>🌍 월드투어</span>
                                <span class="bg-blue-500/20 px-2 py-1 rounded">예정</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>👥 멤버 구성</span>
                                <span class="bg-green-500/20 px-2 py-1 rounded">7명 완전체</span>
                            </div>
                        </div>
                        <div class="mt-4 p-3 bg-gradient-to-r from-purple-500/20 to-blue-500/20 rounded-xl border border-purple-300/30">
                            <p class="text-white/90 text-sm text-center">
                                진, RM, V, 지민, 제이홉, 정국, 슈가 모두 함께하는 완전체 컴백!
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Blackpink News -->
                <div class="group animate-fade-in-up delay-600">
                    <div class="glass-strong rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 hover:scale-105 border border-white/20">
                        <div class="text-5xl mb-4 text-center">🖤</div>
                        <h3 class="text-2xl font-bold text-white mb-4 text-center">Blackpink 로제</h3>
                        <p class="text-white/80 leading-relaxed text-center mb-4">
                            Blackpink 로제가 글로벌 팝스타 브루노 마스와 협업했습니다!
                        </p>
                        <div class="space-y-3 text-white/70 text-sm">
                            <div class="flex items-center justify-between">
                                <span>🎵 신곡 제목</span>
                                <span class="bg-pink-500/20 px-2 py-1 rounded">APT</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>🎤 협업 아티스트</span>
                                <span class="bg-yellow-500/20 px-2 py-1 rounded">브루노 마스</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>🏢 소속사</span>
                                <span class="bg-red-500/20 px-2 py-1 rounded">The Black Label</span>
                            </div>
                        </div>
                        <div class="mt-4 p-3 bg-gradient-to-r from-pink-500/20 to-yellow-500/20 rounded-xl border border-pink-300/30">
                            <p class="text-white/90 text-sm text-center">
                                글로벌 팝스타와의 협업으로 K-팝의 세계적 영향력 재확인!
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Global Impact News -->
                <div class="group animate-fade-in-up delay-800">
                    <div class="glass-strong rounded-3xl p-8 shadow-2xl hover:shadow-3xl transition-all duration-500 hover:scale-105 border border-white/20">
                        <div class="text-5xl mb-4 text-center">🌍</div>
                        <h3 class="text-2xl font-bold text-white mb-4 text-center">글로벌 영향력</h3>
                        <p class="text-white/80 leading-relaxed text-center mb-4">
                            K-팝의 경제적 영향력이 새로운 기록을 세우고 있습니다!
                        </p>
                        <div class="space-y-3 text-white/70 text-sm">
                            <div class="flex items-center justify-between">
                                <span>💰 지적재산권 수지</span>
                                <span class="bg-green-500/20 px-2 py-1 rounded">역대 최고</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>🎵 Spotify 복귀</span>
                                <span class="bg-blue-500/20 px-2 py-1 rounded">카카오와 협상 완료</span>
                            </div>
                            <div class="flex items-center justify-between">
                                <span>📊 글로벌 차트</span>
                                <span class="bg-purple-500/20 px-2 py-1 rounded">전 세계 진출</span>
                            </div>
                        </div>
                        <div class="mt-4 p-3 bg-gradient-to-r from-green-500/20 to-blue-500/20 rounded-xl border border-green-300/30">
                            <p class="text-white/90 text-sm text-center">
                                BTS, Blackpink 경제효과로 한국 문화산업의 글로벌 위상 강화!
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Explore Section -->
        <div class="max-w-2xl mx-auto mb-20 animate-fade-in-up delay-1300">
            <div class="glass-strong rounded-3xl p-8 text-center text-white shadow-2xl animate-glow border border-white/30">
                <h2 class="text-3xl md:text-4xl font-bold mb-4 text-shadow">🎵 K-팝의 매력에 빠져보세요! 🎵</h2>
                <p class="text-xl mb-6 opacity-90">
                    대한민국의 음악이 전 세계를 사로잡는 이유를 직접 경험해보세요
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <button class="glass rounded-full px-8 py-3 font-bold hover:bg-white/20 transition-all duration-300 shadow-lg border border-white/30">
                        🎧 K-팝 플레이리스트
                    </button>
                    <button class="glass rounded-full px-8 py-3 font-bold hover:bg-white/20 transition-all duration-300 shadow-lg border border-white/30">
                        🎬 뮤직비디오 감상
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="glass border-t border-white/20 relative z-10 animate-fade-in-up delay-1400">
        <div class="container mx-auto px-4 py-12">
            <div class="text-center">
                <p class="text-2xl font-bold text-white mb-4 text-shadow">🎵 K-팝의 매력에 빠져보세요! 🎵</p>
                <p class="text-white/70 mb-6">© 2024 K-팝 소개 페이지</p>
                <div class="flex justify-center space-x-4">
                    <div class="w-3 h-3 bg-white rounded-full animate-pulse"></div>
                    <div class="w-3 h-3 bg-white/70 rounded-full animate-pulse" style="animation-delay: 0.2s;"></div>
                    <div class="w-3 h-3 bg-white/50 rounded-full animate-pulse" style="animation-delay: 0.4s;"></div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // 스크롤 기반 애니메이션을 위한 Intersection Observer
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // 페이지 로드 시 모든 애니메이션 요소들을 관찰
        document.addEventListener('DOMContentLoaded', () => {
            const animatedElements = document.querySelectorAll('.animate-fade-in, .animate-fade-in-up, .animate-fade-in-down, .animate-fade-in-left, .animate-fade-in-right');
            animatedElements.forEach(el => {
                observer.observe(el);
            });
        });
    </script>
</body>
</html>
