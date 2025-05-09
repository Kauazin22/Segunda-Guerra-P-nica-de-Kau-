# Segunda-Guerra-Punica-de-Kaua
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Segunda Guerra Púnica - O Confronto entre Roma e Cartago</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .hero-pattern {
            background-image: url('https://images.unsplash.com/photo-1605000797499-95a51c5269ae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80');
            background-size: cover;
            background-position: center;
            background-blend-mode: multiply;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -38px;
            top: 0;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background-color: #d97706;
            border: 4px solid #f59e0b;
        }
        
        .map-container {
            perspective: 1000px;
        }
        
        .map-card {
            transform-style: preserve-3d;
            transition: transform 0.8s;
        }
        
        .map-card:hover {
            transform: rotateY(15deg) rotateX(5deg);
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            animation: fadeIn 1s ease-out forwards;
        }
    </style>
</head>
<body class="bg-amber-50 text-gray-800 font-serif">
    <!-- Navbar -->
    <nav class="bg-amber-900 text-amber-50 shadow-lg sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-helmet-battle text-2xl"></i>
                <span class="text-xl font-bold">Guerra Púnica</span>
            </div>
            <div class="hidden md:flex space-x-6">
                <a href="#sobre" class="hover:text-amber-200 transition">Sobre</a>
                <a href="#timeline" class="hover:text-amber-200 transition">Linha do Tempo</a>
                <a href="#personagens" class="hover:text-amber-200 transition">Personagens</a>
                <a href="#batalhas" class="hover:text-amber-200 transition">Batalhas</a>
                <a href="#legado" class="hover:text-amber-200 transition">Legado</a>
            </div>
            <button class="md:hidden text-xl" id="menuBtn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
        <!-- Mobile Menu -->
        <div class="md:hidden hidden bg-amber-800 px-4 py-2" id="mobileMenu">
            <div class="flex flex-col space-y-3">
                <a href="#sobre" class="hover:text-amber-200 transition">Sobre</a>
                <a href="#timeline" class="hover:text-amber-200 transition">Linha do Tempo</a>
                <a href="#personagens" class="hover:text-amber-200 transition">Personagens</a>
                <a href="#batalhas" class="hover:text-amber-200 transition">Batalhas</a>
                <a href="#legado" class="hover:text-amber-200 transition">Legado</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="hero-pattern bg-amber-700 bg-opacity-70 text-amber-50 py-20">
        <div class="container mx-auto px-4 text-center fade-in">
            <h1 class="text-4xl md:text-6xl font-bold mb-4">Segunda Guerra Púnica</h1>
            <p class="text-xl md:text-2xl mb-8">218 - 201 a.C. • O épico confronto entre Roma e Cartago</p>
            <div class="flex justify-center space-x-4">
                <a href="#sobre" class="bg-amber-600 hover:bg-amber-700 text-white px-6 py-3 rounded-lg font-medium transition shadow-lg">
                    Explorar História
                </a>
                <a href="#batalhas" class="bg-transparent hover:bg-amber-800 text-white border border-white px-6 py-3 rounded-lg font-medium transition">
                    Principais Batalhas
                </a>
            </div>
        </div>
    </header>

    <!-- About Section -->
    <section id="sobre" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-amber-900 mb-4">O Grande Conflito</h2>
                <div class="w-24 h-1 bg-amber-600 mx-auto"></div>
            </div>
            
            <div class="flex flex-col md:flex-row items-center gap-8">
                <div class="md:w-1/2">
                    <img src="https://images.unsplash.com/photo-1605000797499-95a51c5269ae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80" 
                         alt="Antiga batalha romana" 
                         class="rounded-lg shadow-xl w-full h-auto">
                </div>
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-bold text-amber-800 mb-4">A Guerra que Moldou o Mediterrâneo</h3>
                    <p class="text-gray-700 mb-4">
                        A Segunda Guerra Púnica (218-201 a.C.) foi o segundo dos três grandes conflitos entre a República Romana e o Império Cartaginês. Marcada por estratégias ousadas, táticas inovadoras e figuras lendárias, esta guerra redefiniu o equilíbrio de poder no mundo antigo.
                    </p>
                    <p class="text-gray-700 mb-6">
                        O conflito foi desencadeado pelo expansionismo de ambas as potências, com o famoso general cartaginês Aníbal Barca cruzando os Alpes com seus elefantes de guerra para atacar Roma em seu próprio território. A guerra testou os limites de ambas as civilizações e estabeleceu Roma como a principal potência do Mediterrâneo.
                    </p>
                    <div class="bg-amber-100 border-l-4 border-amber-600 p-4">
                        <p class="italic text-amber-900">
                            "Encontrei Roma uma cidade de tijolos e deixei uma cidade de mármore." - Augusto (refletindo sobre o legado das Guerras Púnicas)
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Timeline Section -->
    <section id="timeline" class="py-16 bg-amber-100">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-amber-900 mb-4">Linha do Tempo</h2>
                <div class="w-24 h-1 bg-amber-600 mx-auto"></div>
            </div>
            
            <div class="relative max-w-3xl mx-auto">
                <!-- Timeline line -->
                <div class="absolute left-8 md:left-1/2 h-full w-1 bg-amber-600 transform -translate-x-1/2"></div>
                
                <!-- Timeline items -->
                <div class="space-y-8">
                    <!-- Item 1 -->
                    <div class="relative pl-16 md:pl-0 md:flex justify-between timeline-item">
                        <div class="md:w-5/12 md:pr-8 md:text-right mb-4 md:mb-0">
                            <h3 class="text-xl font-bold text-amber-800">219 a.C.</h3>
                            <p class="text-gray-700">Aníbal ataca Sagunto</p>
                        </div>
                        <div class="md:w-5/12">
                            <div class="bg-white p-6 rounded-lg shadow-md">
                                <p>Aníbal sitia e conquista a cidade de Sagunto, aliada de Roma, desencadeando o conflito. Roma exige a rendição de Aníbal, que é recusada por Cartago.</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Item 2 -->
                    <div class="relative pl-16 md:pl-0 md:flex justify-between timeline-item">
                        <div class="md:w-5/12 order-last">
                            <div class="bg-white p-6 rounded-lg shadow-md">
                                <p>Aníbal lidera seu exército, incluindo elefantes de guerra, através dos Alpes em uma das campanhas militares mais audaciosas da história.</p>
                            </div>
                        </div>
                        <div class="md:w-5/12 md:pl-8 md:text-left mb-4 md:mb-0">
                            <h3 class="text-xl font-bold text-amber-800">218 a.C.</h3>
                            <p class="text-gray-700">Travessia dos Alpes</p>
                        </div>
                    </div>
                    
                    <!-- Item 3 -->
                    <div class="relative pl-16 md:pl-0 md:flex justify-between timeline-item">
                        <div class="md:w-5/12 md:pr-8 md:text-right mb-4 md:mb-0">
                            <h3 class="text-xl font-bold text-amber-800">216 a.C.</h3>
                            <p class="text-gray-700">Batalha de Canas</p>
                        </div>
                        <div class="md:w-5/12">
                            <div class="bg-white p-6 rounded-lg shadow-md">
                                <p>Considerada uma das maiores vitórias táticas da história, Aníbal destrói um exército romano numericamente superior usando uma clássica manobra de cerco.</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Item 4 -->
                    <div class="relative pl-16 md:pl-0 md:flex justify-between timeline-item">
                        <div class="md:w-5/12 order-last">
                            <div class="bg-white p-6 rounded-lg shadow-md">
                                <p>Públio Cornélio Cipião, mais tarde conhecido como Cipião Africano, lidera as forças romanas na Hispânia, cortando as linhas de suprimento de Aníbal.</p>
                            </div>
                        </div>
                        <div class="md:w-5/12 md:pl-8 md:text-left mb-4 md:mb-0">
                            <h3 class="text-xl font-bold text-amber-800">210-206 a.C.</h3>
                            <p class="text-gray-700">Campanhas na Hispânia</p>
                        </div>
                    </div>
                    
                    <!-- Item 5 -->
                    <div class="relative pl-16 md:pl-0 md:flex justify-between timeline-item">
                        <div class="md:w-5/12 md:pr-8 md:text-right mb-4 md:mb-0">
                            <h3 class="text-xl font-bold text-amber-800">202 a.C.</h3>
                            <p class="text-gray-700">Batalha de Zama</p>
                        </div>
                        <div class="md:w-5/12">
                            <div class="bg-white p-6 rounded-lg shadow-md">
                                <p>Cipião derrota Aníbal decisivamente na África, encerrando a guerra. Cartago é forçada a aceitar termos de paz humilhantes, marcando o fim de sua potência militar.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Key Figures Section -->
    <section id="personagens" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-amber-900 mb-4">Personagens Principais</h2>
                <div class="w-24 h-1 bg-amber-600 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Hannibal -->
                <div class="bg-amber-50 rounded-lg overflow-hidden shadow-lg transform transition hover:scale-105">
                    <div class="h-48 bg-amber-700 flex items-center justify-center">
                        <i class="fas fa-chess-king text-6xl text-amber-200"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-2xl font-bold text-amber-900 mb-2">Aníbal Barca</h3>
                        <p class="text-amber-700 font-medium mb-4">General Cartaginês</p>
                        <p class="text-gray-700">
                            Considerado um dos maiores estrategistas militares da história, Aníbal liderou suas forças através dos Alpes e infligiu várias derrotas esmagadoras a Roma, incluindo a lendária Batalha de Canas.
                        </p>
                        <div class="mt-4">
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800 mr-2">Estratégia</span>
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800 mr-2">Coragem</span>
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800">Liderança</span>
                        </div>
                    </div>
                </div>
                
                <!-- Scipio -->
                <div class="bg-amber-50 rounded-lg overflow-hidden shadow-lg transform transition hover:scale-105">
                    <div class="h-48 bg-amber-700 flex items-center justify-center">
                        <i class="fas fa-shield-alt text-6xl text-amber-200"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-2xl font-bold text-amber-900 mb-2">Cipião Africano</h3>
                        <p class="text-amber-700 font-medium mb-4">General Romano</p>
                        <p class="text-gray-700">
                            O único general romano a derrotar Aníbal em batalha. Adotou táticas cartaginesas contra eles mesmos e levou a guerra para a África, forçando Aníbal a retornar e enfrentá-lo em Zama.
                        </p>
                        <div class="mt-4">
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800 mr-2">Adaptabilidade</span>
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800 mr-2">Visão</span>
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800">Inovação</span>
                        </div>
                    </div>
                </div>
                
                <!-- Fabius -->
                <div class="bg-amber-50 rounded-lg overflow-hidden shadow-lg transform transition hover:scale-105">
                    <div class="h-48 bg-amber-700 flex items-center justify-center">
                        <i class="fas fa-hourglass-half text-6xl text-amber-200"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-2xl font-bold text-amber-900 mb-2">Fábio Máximo</h3>
                        <p class="text-amber-700 font-medium mb-4">Ditador Romano</p>
                        <p class="text-gray-700">
                            Conhecido como "O Temporizador", adotou uma estratégia de terra arrasada e guerrilha contra Aníbal, evitando confrontos diretos. Suas táticas foram cruciais para desgastar o exército cartaginês.
                        </p>
                        <div class="mt-4">
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800 mr-2">Paciência</span>
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800 mr-2">Resiliência</span>
                            <span class="inline-block bg-amber-200 rounded-full px-3 py-1 text-sm font-semibold text-amber-800">Sabedoria</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Battles Section -->
    <section id="batalhas" class="py-16 bg-amber-800 text-amber-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">Batalhas Decisivas</h2>
                <div class="w-24 h-1 bg-amber-300 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <!-- Trebia -->
                <div class="bg-amber-900 rounded-lg overflow-hidden shadow-xl">
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-2">Batalha do Trébia</h3>
                        <p class="text-amber-300 font-medium mb-4">Dezembro de 218 a.C.</p>
                        <p class="mb-4">
                            A primeira grande batalha na Itália, onde Aníbal usou o terreno e emboscadas para derrotar um exército romano numericamente superior. Demonstrou sua superioridade tática e a vulnerabilidade das legiões romanas tradicionais.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold mr-2">Cartago: 20,000</span>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold">Roma: 42,000</span>
                            </div>
                            <button class="bg-amber-700 hover:bg-amber-600 px-4 py-2 rounded-lg transition battle-detail-btn" data-battle="trebia">
                                Detalhes <i class="fas fa-chevron-right ml-1"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Lake Trasimene -->
                <div class="bg-amber-900 rounded-lg overflow-hidden shadow-xl">
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-2">Batalha do Lago Trasimeno</h3>
                        <p class="text-amber-300 font-medium mb-4">Junho de 217 a.C.</p>
                        <p class="mb-4">
                            Uma emboscada magistral onde Aníbal destruiu um exército romano inteiro, matando cerca de 15,000 legionários. Foi a maior emboscada da história militar antiga e consolidou a reputação de Aníbal como gênio militar.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold mr-2">Cartago: 50,000</span>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold">Roma: 30,000</span>
                            </div>
                            <button class="bg-amber-700 hover:bg-amber-600 px-4 py-2 rounded-lg transition battle-detail-btn" data-battle="trasimeno">
                                Detalhes <i class="fas fa-chevron-right ml-1"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Cannae -->
                <div class="bg-amber-900 rounded-lg overflow-hidden shadow-xl">
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-2">Batalha de Canas</h3>
                        <p class="text-amber-300 font-medium mb-4">2 de Agosto de 216 a.C.</p>
                        <p class="mb-4">
                            O auge do gênio tático de Aníbal, onde seu exército menor cercou e aniquilou um exército romano duas vezes maior. Cerca de 70,000 romanos morreram - uma das piores derrotas da história militar romana.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold mr-2">Cartago: 50,000</span>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold">Roma: 86,000</span>
                            </div>
                            <button class="bg-amber-700 hover:bg-amber-600 px-4 py-2 rounded-lg transition battle-detail-btn" data-battle="cannae">
                                Detalhes <i class="fas fa-chevron-right ml-1"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Zama -->
                <div class="bg-amber-900 rounded-lg overflow-hidden shadow-xl">
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-2">Batalha de Zama</h3>
                        <p class="text-amber-300 font-medium mb-4">19 de Outubro de 202 a.C.</p>
                        <p class="mb-4">
                            O confronto final entre Aníbal e Cipião Africano. Cipião usou táticas aprendidas com os cartagineses para derrotar Aníbal decisivamente, encerrando a guerra. Marcou o fim de Cartago como potência militar.
                        </p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold mr-2">Cartago: 40,000</span>
                                <span class="inline-block bg-amber-700 rounded-full px-3 py-1 text-sm font-semibold">Roma: 35,000</span>
                            </div>
                            <button class="bg-amber-700 hover:bg-amber-600 px-4 py-2 rounded-lg transition battle-detail-btn" data-battle="zama">
                                Detalhes <i class="fas fa-chevron-right ml-1"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Map Section -->
    <section class="py-16 bg-amber-100">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-amber-900 mb-4">Campanhas e Movimentações</h2>
                <div class="w-24 h-1 bg-amber-600 mx-auto"></div>
            </div>
            
            <div class="map-container">
                <div class="map-card bg-white rounded-xl shadow-2xl overflow-hidden max-w-4xl mx-auto">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Second_Punic_War_218-202_BC-fr.svg/1200px-Second_Punic_War_218-202_BC-fr.svg.png" 
                         alt="Mapa das campanhas da Segunda Guerra Púnica" 
                         class="w-full h-auto">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-amber-900 mb-2">O Teatro de Guerra</h3>
                        <p class="text-gray-700">
                            A Segunda Guerra Púnica foi travada em três continentes: Europa, África e Ásia. O mapa mostra as principais rotas de Aníbal da Hispânia através dos Alpes até a Itália, bem como as campanhas romanas na Hispânia e o ataque final à África.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Legacy Section -->
    <section id="legado" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-amber-900 mb-4">Legado e Consequências</h2>
                <div class="w-24 h-1 bg-amber-600 mx-auto"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-amber-50 p-6 rounded-lg shadow-md">
                    <div class="text-amber-700 text-4xl mb-4">
                        <i class="fas fa-globe-europe"></i>
                    </div>
                    <h3 class="text-xl font-bold text-amber-900 mb-2">Ascensão de Roma</h3>
                    <p class="text-gray-700">
                        A vitória estabeleceu Roma como a potência dominante no Mediterrâneo ocidental, pavimentando o caminho para sua eventual dominação de todo o mundo mediterrâneo.
                    </p>
                </div>
                
                <div class="bg-amber-50 p-6 rounded-lg shadow-md">
                    <div class="text-amber-700 text-4xl mb-4">
                        <i class="fas fa-city"></i>
                    </div>
                    <h3 class="text-xl font-bold text-amber-900 mb-2">Declínio de Cartago</h3>
                    <p class="text-gray-700">
                        Cartago foi reduzida a um estado cliente de Roma, perdendo seu império ultramarino e pagando pesadas indenizações. A destruição final viria na Terceira Guerra Púnica.
                    </p>
                </div>
                
                <div class="bg-amber-50 p-6 rounded-lg shadow-md">
                    <div class="text-amber-700 text-4xl mb-4">
                        <i class="fas fa-chess"></i>
                    </div>
                    <h3 class="text-xl font-bold text-amber-900 mb-2">Inovações Militares</h3>
                    <p class="text-gray-700">
                        A guerra revolucionou a arte da guerra romana, levando à adoção de táticas mais flexíveis e à profissionalização do exército. As lições aprendidas com Aníbal moldaram o exército romano por séculos.
                    </p>
                </div>
            </div>
            
            <div class="mt-12 bg-amber-100 border-l-4 border-amber-600 p-6 rounded-lg max-w-3xl mx-auto">
                <h3 class="text-xl font-bold text-amber-900 mb-2">Por que estudar a Segunda Guerra Púnica?</h3>
                <p class="text-gray-700">
                    Este conflito oferece lições atemporais sobre estratégia, liderança, resiliência e as consequências imprevistas da guerra. As táticas de Aníbal em Canas ainda são estudadas em academias militares, enquanto a resposta romana ao desastre mostra a importância da adaptabilidade institucional.
                </p>
            </div>
        </div>
    </section>

    <!-- Battle Modals -->
    <div id="battleModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
        <div class="bg-white rounded-lg shadow-xl max-w-2xl w-full max-h-[90vh] overflow-y-auto">
            <div class="p-6">
                <div class="flex justify-between items-start mb-4">
                    <h3 id="modalBattleTitle" class="text-2xl font-bold text-amber-900"></h3>
                    <button id="closeModal" class="text-gray-500 hover:text-gray-700">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                <div id="modalBattleContent" class="text-gray-700 space-y-4">
                    <!-- Content will be inserted here by JavaScript -->
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-amber-900 text-amber-100 py-8">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <div class="flex items-center space-x-2">
                        <i class="fas fa-helmet-battle text-2xl"></i>
                        <span class="text-xl font-bold">Segunda Guerra Púnica</span>
                    </div>
                    <p class="mt-2 text-amber-200">Explorando um dos conflitos mais fascinantes da antiguidade</p>
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="hover:text-amber-300 transition"><i class="fab fa-twitter text-xl"></i></a>
                    <a href="#" class="hover:text-amber-300 transition"><i class="fab fa-facebook text-xl"></i></a>
                    <a href="#" class="hover:text-amber-300 transition"><i class="fab fa-instagram text-xl"></i></a>
                </div>
            </div>
            <div class="border-t border-amber-800 mt-6 pt-6 text-center text-amber-300">
                <p>&copy; 2023 História Antiga. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const menuBtn = document.getElementById('menuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        
        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    mobileMenu.classList.add('hidden');
                }
            });
        });
        
        // Battle modal functionality
        const battleModal = document.getElementById('battleModal');
        const modalTitle = document.getElementById('modalBattleTitle');
        const modalContent = document.getElementById('modalBattleContent');
        const closeModal = document.getElementById('closeModal');
        
        const battleDetails = {
            trebia: {
                title: "Batalha do Trébia",
                content: `
                    <p><strong>Local:</strong> Rio Trébia, norte da Itália</p>
                    <p><strong>Comandantes:</strong> Aníbal Barca (Cartago) vs. Tibério Semprônio Longo (Roma)</p>
                    <p><strong>Resultado:</strong> Vitória cartaginesa decisiva</p>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">Táticas de Aníbal:</h4>
                        <p>Aníbal usou o terreno para canalizar as forças romanas, enquanto sua cavalaria e uma força oculta atacavam os flancos e retaguarda. A batalha demonstrou a superioridade da cavalaria cartaginesa e a vulnerabilidade das formações romanas tradicionais.</p>
                    </div>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">Consequências:</h4>
                        <p>A derrota chocou Roma e provou que Aníbal era uma ameaça séria. Os romanos começaram a perceber que precisavam adaptar suas táticas para enfrentar o gênio militar cartaginês.</p>
                    </div>
                `
            },
            trasimeno: {
                title: "Batalha do Lago Trasimeno",
                content: `
                    <p><strong>Local:</strong> Lago Trasimeno, Itália central</p>
                    <p><strong>Comandantes:</strong> Aníbal Barca (Cartago) vs. Caio Flamínio (Roma)</p>
                    <p><strong>Resultado:</strong> Vitória cartaginesa esmagadora</p>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">A Emboscada:</h4>
                        <p>Aníbal posicionou suas tropas nas colinas ao redor do estreito caminho ao longo do lago. Quando o exército romano marchou pelo desfiladeiro em formação de marcha, os cartagineses atacaram de todos os lados simultaneamente.</p>
                    </div>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">Impacto:</h4>
                        <p>Foi a pior derrota romana até então, com cerca de 15,000 mortos. A batalha levou à nomeação de Fábio Máximo como ditador e sua estratégia de evitar confrontos diretos com Aníbal.</p>
                    </div>
                `
            },
            cannae: {
                title: "Batalha de Canas",
                content: `
                    <p><strong>Local:</strong> Canas, Itália sudeste</p>
                    <p><strong>Comandantes:</strong> Aníbal Barca (Cartago) vs. Lúcio Emílio Paulo e Caio Terêncio Varrão (Roma)</p>
                    <p><strong>Resultado:</strong> Vitória cartaginesa catastrófica para Roma</p>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">A Manobra de Cerco:</h4>
                        <p>Aníbal formou um semicírculo convexo que se transformou em côncavo quando os romanos avançaram. Suas tropas experientes nas laterais envolveram os romanos enquanto a cavalaria atacava pela retaguarda, cercando completamente o exército romano.</p>
                    </div>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">Legado:</h4>
                        <p>Canas permanece como um exemplo clássico de batalha de aniquilação. Apesar da vitória, Aníbal não conseguiu capitalizar estrategicamente, pois Roma se recusou a negociar e continuou a guerra.</p>
                    </div>
                `
            },
            zama: {
                title: "Batalha de Zama",
                content: `
                    <p><strong>Local:</strong> Zama Regia, norte da África</p>
                    <p><strong>Comandantes:</strong> Cipião Africano (Roma) vs. Aníbal Barca (Cartago)</p>
                    <p><strong>Resultado:</strong> Vitória romana decisiva</p>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">A Virada:</h4>
                        <p>Cipião usou formações mais abertas para neutralizar os elefantes de guerra de Aníbal e manobrou suas tropas para evitar ser flanqueado. A superioridade da cavalaria romana, reforçada pelo rei númida Masinissa, foi decisiva.</p>
                    </div>
                    <div class="bg-amber-100 p-4 rounded-lg">
                        <h4 class="font-bold text-amber-800 mb-2">Consequências:</h4>
                        <p>Cartago foi forçada a se render, perdendo todas as possessões ultramarinas, sua frota e pagando enormes reparações. A vitória estabeleceu Roma como a potência dominante no Mediterrâneo ocidental.</p>
                    </div>
                `
            }
        };
        
        document.querySelectorAll('.battle-detail-btn').forEach(button => {
            button.addEventListener('click', () => {
                const battleId = button.getAttribute('data-battle');
                const battle = battleDetails[battleId];
                
                modalTitle.textContent = battle.title;
                modalContent.innerHTML = battle.content;
                
                battleModal.classList.remove('hidden');
                document.body.style.overflow = 'hidden';
            });
        });
        
        closeModal.addEventListener('click', () => {
            battleModal.classList.add('hidden');
            document.body.style.overflow = '';
        });
        
        battleModal.addEventListener('click', (e) => {
            if (e.target === battleModal) {
                battleModal.classList.add('hidden');
                document.body.style.overflow = '';
            }
        });
        
        // Animate elements on scroll
        const observerOptions = {
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
