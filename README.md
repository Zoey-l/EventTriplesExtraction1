# EventTriplesExtraction
&nbsp;&nbsp;EventTriplesExtraction based on dependency parser and semantic role labeling, 基于依存句法与语义角色标注的事件三元组抽取
&nbsp;&nbsp;  
   本项目从事件三元组的方式出发，对文本进行表示．

# 使用方式

        from triples_extraction import *
        extractor = TripleExtractor()
        svos = extractor.triples_main(content)
        print('svos', svos)

# 测试样例
        content = '李克强总理今天来我家了,我感到非常荣幸'
        svos = [
                  ['李克强总理', '来', '我家'],
                  ['我', '感到', '荣幸']
                 ]

        content = ''' 以色列国防军20日对加沙地带实施轰炸，造成3名巴勒斯坦武装人员死亡。此外，巴勒斯坦人与以色列士兵当天在加沙地带与以交界地区发生冲突，一名巴勒斯坦人被打死。当天的冲突还造成210名巴勒斯坦人受伤。
    当天，数千名巴勒斯坦人在加沙地带边境地区继续“回归大游行”抗议活动。部分示威者燃烧轮胎，并向以军投掷石块、燃烧瓶等，驻守边境的以军士兵向示威人群发射催泪瓦斯并开枪射击。'''
        svos = [
                 ['以色列国防军', '实施', '轰炸'],
                 ['冲突', '发生', '巴勒斯坦人与以色列士兵'],
                 ['当天冲突', '造成', '受伤'],
                 ['数千名巴勒斯坦人', '继续', '回归大游行抗议活动'],
                 ['部分示威者', '投掷', '石块'],
                 ['驻守边境以军士兵', '发射', '催泪瓦斯']
                 ]
