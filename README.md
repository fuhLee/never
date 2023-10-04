import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack{
        VStack{
        HStack{
            HStack{
        Text("聊天")
            .foregroundColor(.white)
        .padding()
        Spacer()
                Image(systemName: "bubble.right")
                    .resizable()
                    .scaledToFill()
                    .frame(width: 0, height: 20)
                    .foregroundColor(.white)
                    .padding()
                Image(systemName: "ellipses.bubble")
                    .resizable()
                    .scaledToFill()
                    .frame(width: 0, height: 20)
                    .foregroundColor(.white)
                    .padding()
         Image(systemName: "ellipsis")
            .resizable()
            .scaledToFill()
            .frame(width: 20, height: 4)
            .foregroundColor(.white)
            .rotation3DEffect(
                .degrees(-90), axis: (x: 0, y: 0, z: 0.5)
            )
        }
            .background(Color.black)
          
            
        }
        }
            
                HStack( spacing: 3){
                    Text(" ")
                        Image(systemName: "magnifyingglass")
                            .resizable()
                            .scaledToFill()
                            .frame(width: 10, height: 10)
                            .foregroundColor(.white)
                            .clipped()
                Text("搜尋")
                    .foregroundColor(.white)
                   Spacer()
                    Image(systemName: "viewfinder")
                        .resizable()
                        .scaledToFill()
                        .frame(width: 20, height: 20)
                        .foregroundColor(.white)
                    Text(" ")
            }
               
                .frame(width: 310, height: 25)
                .background(Color.secondary)
                .clipShape(RoundedRectangle(cornerRadius: 5))

               
            VStack{
                ExtractedView(icon: "moon.stars",name: "天天不睡覺(399)     ",bount: "昨天到今天都還醒著",system: "speaker.slash",test: "21:00",mm: "14")
                    .padding(4)
                ExtractedView(icon: "tropicalstorm",name: "颱風報班團(12)",bount: "小犬要來了",system: "speaker.slash",test: "17:22",mm: "30")
                    .padding(4)
                ExtractedView(icon: "sun.dust.fill",name: "日出真美麗（０)",bount: "現在還有人醒著嗎",system: "xmark.octagon",test: " 3:26",mm: "")
                    .padding(4)
                ExtractedView(icon: "gamecontroller",name: "水瓶的小小心電感應（４９）",bount: "今天考的在昨天有寫過感恩   ",system: "speaker.slash",test: "01:11 ",mm: "51")
                    .padding(4)
                
                ExtractedView(icon: "app.gift.fill",name: "聖１２們聚會    (12)",bount: "要在聖誕節前離開嗎",system: "speaker.slash",test: " 昨天 ",mm: "44")
                    .padding(5)
                ExtractedView(icon: "app.gift.fill",name: "聖１２們聚會    (13)",bount: "要在聖誕節前離開嗎",system: "speaker.slash",test: " 昨天 ",mm: "04")
                    .padding(5)
                
            }
            
            
            
        HStack{
            VStack{
                   Image(systemName: "house.fill")
                    .resizable()
                    .scaledToFill()
                    .frame(width: 0,height: 15)
                    .foregroundColor(.white)
                Button("主頁"){
                }
                .font(.system(size: 12))
                .foregroundColor(.white)
            }
                        .padding(6)
            Spacer()
            VStack{
                   Image(systemName: "text.bubble.fill")
                    .resizable()
                    .scaledToFill()
                    .frame(width: 0,height: 15)
                    .foregroundColor(.white)
                Button("聊天"){
                }
                .font(.system(size: 12))
                .foregroundColor(.white)
            }
                        .padding(6)
            Spacer()
            VStack{
                   Image(systemName: "play.circle")
                    .resizable()
                    .scaledToFill()
                    .frame(width: 0,height: 15)
                    .foregroundColor(.white)
                Button("VOOM"){
                }
                .font(.system(size: 12))
                .foregroundColor(.white)
            }
                        .padding()
            Spacer()
                        
            VStack{
                   Image(systemName: "cloud.moon")
                    .resizable()
                    .scaledToFill()
                    .frame(width: 0,height: 15)
                    .foregroundColor(.white)
                Button("TODAY"){
                }
                .font(.system(size: 12))
                .foregroundColor(.white)
            }
                        .padding()
            Spacer()
            
            VStack{
                   Image(systemName: "creditcard.fill")
                    .resizable()
                    .scaledToFill()
                    .frame(width: 0,height: 15)
                    .foregroundColor(.white)
                Button("錢包"){
                }
                .font(.system(size: 12))
                .foregroundColor(.white)
            }
                        .padding()
            Spacer()
                    }
        
        .background(Color.black)
        .shadow(radius: 10)
    }
}
}
struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}



struct ExtractedView: View {
    let icon: String
    let name: String
    let bount: String
    let system: String
    let test: String
    let mm: String
    var body: some View {
        
        HStack(){
            
            Image(systemName:icon)
                .resizable()
                .scaledToFill()
                .frame(width: 30, height: 30)
                .clipShape(Circle())
            VStack{
                HStack{
            Text(name)
                .font(.system(size: 12))
                   
                }
                Button(bount){
                }
                .font(.system(size: 12))
               
                
            }
           
            VStack{
            Image(systemName:system)
                .resizable()
                .scaledToFill()
                .frame(width: 12, height: 12)
                Text(" ")
                    .frame(width: 5, height: 5)
            }
            Spacer()
            VStack{
            Text(test)
                .font(.system(size: 11))
                .padding(2)
                .foregroundColor(.pink)
                Text(mm)
                    .font(.system(size: 15))
                    .foregroundColor(.white)
                    .background(Color.gray)
                    .clipShape(Circle())
                    .padding(2)
                    
            }
        }
      
    }
}
